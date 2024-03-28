## Architecture Overview

### Basic Architecture

![Basic Architecture](https://shorturl.at/acjxY)

This architecture diagram represents the core components and functionalities of the Renix Document Processing API. The API is built using the FastAPI web framework, which serves as the entry point and handles the incoming requests and responses.

#### Utilities

- **DynamoDB:** Integration with Amazon DynamoDB for data storage and retrieval.
- **AzureKeyVault:** Integration with Azure Key Vault for secure secret management.
- **Logger:** Logging utility for logging and debugging purposes.

The central component of this architecture is the DOCX class, which encapsulates the core document processing functionalities. The DOCX class consists of the following methods and functionalities:
1. init_object: 
2. file_to_attribute_extraction
3. document_slicing
4. document_deduplication_doc
5. document_deduplication_page
6. upload_file_to_attribute_extraction 
7. upload_document_slicing 
8. upload_document_deduplication_doc 
9. upload_document_deduplication_page 

The architecture diagram shows that the FastAPI component utilizes the DOCX class and the various utility components to perform document processing tasks based on the incoming requests. The "uses" arrow indicates that the FastAPI component relies on the functionalities provided by the DOCX class and the utility components to carry out its operations.


### Low level design architecture

![Low level design architecture](https://shorturl.at/dfim8)

This architecture diagram represents the overall structure and components of the Renix Document Processing API built using FastAPI. It includes components such as Main, DocumentAnalyseRequest, DocumentAnalyseResponse, ErrorResponse, SuccessResponse, DOCX, and Utilities.

# Architecture Overview

## Main
- This component represents the main entry point of the API.
- It contains various routes for handling different document processing tasks, such as:
  - `hello()`: A simple hello world route.
  - `login()`: Route for handling user login requests.
  - `attribute_extraction_async()`: Asynchronous route for attribute extraction from documents.
  - `attribute_extraction_sync()`: Synchronous route for attribute extraction from documents.
  - `handle_document_slicing()`: Route for handling document slicing tasks.
  - `handle_document_deduplication_doc()`: Route for document deduplication at the document level.
  - `handle_document_deduplication_page()`: Route for document deduplication at the page level.
- Additionally, there are corresponding routes with the "upload" prefix (e.g., `upload_attribute_extraction_async()`, `upload_handle_document_slicing()`, etc.) for handling file uploads related to the respective tasks.

## DocumentAnalyseRequest
- This component represents the data model or request body for document analysis requests.
- It likely contains fields such as `folder_location` and `file_locations` to specify the input documents or folders for processing.

## DocumentAnalyseResponse
- This component represents the response data model for document analysis requests.
- It may contain fields like `request_id`, `folder_location`, `file_locations`, and `status` to provide information about the processing request and its status.

## ErrorResponse
- This component represents the error response data model.
- It likely includes fields like `timestamp`, `request_id`, and `error` to provide information about the error that occurred during processing.

## SuccessResponse
- This component represents the success response data model.
- It may include fields like `timestamp` and `request_id` to indicate a successful processing request.

## DOCX
- This component represents the core class responsible for performing various document processing operations.
- It includes methods such as `init_object()`, `file_to_attribute_extraction()`, `document_slicing()`, `document_deduplication_doc()`, `document_deduplication_page()`, and their corresponding "upload" variants for handling file uploads.

## Utilities
- `logger`: This component represents a logging utility used for logging and debugging purposes throughout the application.
- `AzureKeyVault`: This component represents the integration with Azure Key Vault for securely managing and retrieving secrets, such as API keys or database credentials.
- `config (Settings)`: This component likely represents the configuration settings or environment variables used by the application.
- `admin_client_functions (router)`: This component may represent additional routes and functions related to administrative or client-specific operations.
- `db (DynamoDB)`: This component represents the integration with Amazon DynamoDB, a NoSQL database service, likely used for storing and retrieving data related to document processing tasks.

The diagram shows the relationships and interactions between the various components. The Main component interacts with the DOCX class and the utility components to handle incoming requests and perform document processing tasks. The data models (DocumentAnalyseRequest, DocumentAnalyseResponse, ErrorResponse, SuccessResponse) are used for request and response data formatting.



