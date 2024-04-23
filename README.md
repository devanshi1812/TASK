# TASK
File System
To run this application locally, follow these steps:

1.Clone the repository to your local machine:
git clone <repository-url>
2.Navigate into the project directory:
cd secure-file-sharing-backend
3.Install dependencies using npm or yarn:
npm install
yarn install
4.Start the server:
yarn start
The server should now be running locally on port 3000.
API Endpoints
The following API endpoints are available:

1.Register User
Method: POST
Endpoint: /register
Description: Allows users to register by providing a username.
Request Body: { "username": "example_user" }
Response: { "message": "User registered successfully" }
2.Create Encrypted File
Method: POST
Endpoint: /file/create
Description: Allows users to create an encrypted file by providing the text content.
Request Body: { "content": "plain_text_content" }
Response: { "message": "File created successfully" }
3.Add User to File
Method: PUT
Endpoint: /file/:fileId/adduser
Description: Allows users to add other users to access the encrypted file.
Request Parameters: fileId (ID of the encrypted file)
Request Body: { "username": "username_to_add" }
Response: { "message": "User added successfully" }
4.View All Files
Method: GET
Endpoint: /files
Description: Allows users to view all encrypted files created by all users. Only files shared with the user or created by the user will be decrypted and visible in plain text.
Response: Array of encrypted files objects
