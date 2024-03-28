### API ROUTES:

1. **GET /hello:**
   - This route is a simple "Hello, World!" endpoint used for testing purposes.
   - It returns a message greeting the user.

2. **POST /login:**
   - This route handles user authentication and login requests.
   - It accepts a LoginRequest object containing the user's email and password.
   - Upon successful authentication, it generates and returns a JSON Web Token (JWT) as an access token.

3. **POST /document/attribute-extraction-async:**
   - This route handles asynchronous attribute extraction requests for documents.
   - It accepts a DocumentAnalyseRequest object, which can contain either a folder_location or a list of file_locations.
   - The attribute extraction process is offloaded to a background task, and a SuccessResponse with a request ID is returned immediately.

4. **POST /document/attribute-extraction-sync:**
   - This route handles synchronous attribute extraction requests for documents.
   - It accepts a DocumentAnalyseRequest object, similar to the asynchronous variant.
   - The attribute extraction is performed synchronously, and the results are returned directly.

5. **POST /document/document-slicing:**
   - This route handles document slicing requests, where a document is divided into smaller parts or sections.
   - It accepts a DocumentAnalyseRequest object with either a folder_location or a list of file_locations.
   - The document slicing results are returned directly.

6. **POST /document/deduplication-doc:**
   - This route handles document-level deduplication requests, where two entire documents are compared for duplicates.
   - It accepts a DocumentDeduplicationDocRequest object containing the locations of the two files to be compared.
   - The deduplication results are returned directly.

7. **POST /document/deduplication-page:**
   - This route handles page-level deduplication requests, where the pages within a document are compared for duplicates.
   - It accepts a DocumentDeduplicationPageRequest object containing the location of the file to be processed.
   - The deduplication results are returned directly.

8. **POST /document/upload/attribute-extraction-async:**
   - This route handles asynchronous attribute extraction requests for uploaded files.
   - It accepts an UploadFile object containing the file to be processed.
   - The attribute extraction process is offloaded to a background task, and a SuccessResponse with a request ID is returned immediately.

9. **POST /document/upload/attribute-extraction-sync:**
   - This route handles synchronous attribute extraction requests for uploaded files.
   - It accepts an UploadFile object containing the file to be processed.
   - The attribute extraction is performed synchronously, and the results are returned directly.

10. **POST /document/upload/document-slicing:**
    - This route handles document slicing requests for uploaded files.
    - It accepts an UploadFile object containing the PDF file to be processed.
    - The document slicing results are returned directly.

11. **POST /document/upload/deduplication-doc:**
    - This route handles document-level deduplication requests for uploaded files.
    - It accepts two UploadFile objects containing the PDF files to be compared.
    - The deduplication results are returned directly.

12. **POST /document/upload/deduplication-page:**
    - This route handles page-level deduplication requests for uploaded files.
    - It accepts an UploadFile object containing the PDF file to be processed.
    - The deduplication results are returned directly.
