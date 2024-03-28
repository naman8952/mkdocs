## Configuration:

### Configuration Settings for Renix Document Processing API:

The Renix Document Processing API utilizes configuration files to manage different environments. Below are the configuration parameters and their default values:

1. **General Settings:**
   - `app_name`: The name of the application.
   - `aws_dynamodb_region`: The AWS region for DynamoDB.
   - `aws_dynamodb_table`: The name of the DynamoDB table.
   - `parallel_threads`: Number of parallel threads for processing.
   - `client_table`: Name of the client table.
   - `azure_key_vault_name`: The name of Azure Key Vault.
   - `access_token_expire_hours`: Expiry duration for access tokens (in hours).
   - `upload_file_size_limit_in_mb`: Maximum file size limit for uploads (in megabytes).

2. **Environment-specific Settings:**
   - **Development Environment** (.dev):
     - Include details about the configuration specific to the development environment, such as environment variables or file paths.
   - **Production Environment** (.prod):
     - Include details about the configuration specific to the production environment, such as API keys or database credentials.
   - **Quality Assurance Environment** (.qa):
     - Include details about the configuration specific to the QA environment, such as test endpoints or debug settings.
