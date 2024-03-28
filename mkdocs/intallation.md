## Installation and Setup

### Installation Instructions:

1. **Ensure Python 3.9 is Installed:** Make sure you have Python 3.9 installed on your system.

2. **Install Dependencies:**
```bash
   pip install -r requirements.txt
```
3.**Running the Application for Development:**

To run the application for development purposes, execute the following command:
```bash
      python main.py -d
```
4.**Running Unit Tests:**

To run unit tests for the API, follow these steps:
   
 1.**Ensure you have configured your environment using the appropriate .env file. For example:**

```
pytest --envfile configs/.env.dev
```
Replace configs/.env.dev with the path to your environment configuration file.

2.**Execute the following command to run the unit tests:**


```
pytest --envfile configs/.env.dev
```
This command will execute all unit tests, validating the functionality of the Renix Document Processing API.



