## Utilities:

The project utilizes several utility components to assist with various tasks. Here's a brief overview of these utilities:

1. **DynamoDB:**
   - This utility component is responsible for interacting with Amazon DynamoDB, a NoSQL database service provided by AWS.
   - It is used for storing and retrieving data related to document processing requests, client information, and other application data.
   - The `DynamoDB` class likely provides methods for adding, updating, and retrieving items from DynamoDB tables.
   - It is instantiated with configuration settings, such as the AWS DynamoDB table name, and is used throughout the application to persist and retrieve data.

2. **AzureKeyVault:**
   - This utility component is used for securely managing and retrieving secrets, such as the JWT secret key (`JWT_SECRET_KEY`).
   - It interacts with Azure Key Vault, a cloud service provided by Microsoft Azure for securely storing and accessing secrets, keys, and certificates.
   - The `AzureKeyVault` class likely provides methods for retrieving secrets from the Azure Key Vault instance.
   - It is used in the `create_access_token` function to obtain the JWT secret key for signing and verifying JSON Web Tokens (JWTs).

3. **logger:**
   - This utility component is responsible for logging and debugging within the application.
   - The `logger` object is used throughout the application to log messages at different levels (e.g., info, debug, warning, error), providing valuable information for debugging and monitoring purposes.
   - The logged messages can be written to various destinations, such as the console, log files, or remote logging services, depending on the configuration.

