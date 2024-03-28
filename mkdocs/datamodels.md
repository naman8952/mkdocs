## Data Models:

The project uses several data models, implemented as Pydantic models, for representing requests, responses, and other data structures. Here's a description of the main data models and their fields:

1. **DocumentAnalyseRequest:**
   - **Purpose:** Represents a request for document analysis operations.
   - **Fields:**
     - `folder_location` (str, optional): The location of a folder containing documents to be analyzed.
     - `file_locations` (List[str], optional): A list of file locations for documents to be analyzed.

2. **DocumentAnalyseResponse:**
   - **Purpose:** Represents the response for a document analysis request.
   - **Fields:**
     - `request_id` (str): A unique identifier for the request.
     - `folder_location` (str, optional): The location of the folder containing the analyzed documents (if provided in the request).
     - `file_locations` (List[str], optional): The list of file locations for the analyzed documents (if provided in the request).
     - `status` (str): The current status of the document analysis request.

3. **DocumentDeduplicationDocRequest:**
   - **Purpose:** Represents a request for document-level deduplication, comparing two entire documents.
   - **Fields:**
     - `file_location1` (str): The location of the first file to be compared.
     - `file_location2` (str): The location of the second file to be compared.

4. **DocumentDeduplicationPageRequest:**
   - **Purpose:** Represents a request for page-level deduplication within a document.
   - **Fields:**
     - `file_location` (str): The location of the file for which page-level deduplication is requested.

5. **ErrorResponse:**
   - **Purpose:** Represents an error response from the API.
   - **Fields:**
     - `timestamp` (str): The timestamp when the error occurred.
     - `request_id` (str): The unique identifier for the request that caused the error.
     - `error` (dict): A dictionary containing details about the error, including the code, message, and trace.

6. **SuccessResponse:**
   - **Purpose:** Represents a successful response from the API.
   - **Fields:**
     - `timestamp` (str): The timestamp when the successful response was generated.
     - `request_id` (str): The unique identifier for the successful request.

7. **Error:**
   - **Purpose:** Represents an error object used within the ErrorResponse model.
   - **Fields:**
     - `code` (str): A code representing the type of error.
     - `message` (str): A human-readable message describing the error.
     - `trace` (str): A trace or stack trace related to the error (if available).

8. **LoginRequest:**
   - **Purpose:** Represents a request for user authentication and login.
   - **Fields:**
     - `email` (str): The user's email address.
     - `password` (str): The user's password.

9. **ErrorLoginResponse:**
   - **Purpose:** Represents an error response for a failed login attempt.
   - **Fields:**
     - `message` (str): A message describing the error or reason for the failed login.

10. **Token:**
    - **Purpose:** Represents an authentication token issued upon successful login.
    - **Fields:**
      - `access_token` (str): The JWT access token.
      - `token_type` (str): The type of the token (e.g., "bearer").

11. **TokenData:**
    - **Purpose:** Represents the data contained within a JWT token.
    - **Fields:**
      - `clientId` (str, optional): The ID of the authenticated client.
      - `email` (str, optional): The email address of the authenticated user.
      - `clientName` (str, optional): The name of the authenticated client.

These data models are used throughout the API for handling requests, responses, and representing various data structures related to document processing, authentication, and error handling.
