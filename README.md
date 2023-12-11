# ITIS_6177_Final_Project- Computer Vision API - Optical Character Recognition

A simple OCR Application using Computer Vision API. OCR(Optical Character Recognition) converting images with printed or handwritten text into machine-encoded text.

Application URL:- http://64.176.215.214:3000/


To create an API on Microsoft Azure:

1. Create an account and log in to the Azure portal.
2. Create a new resource to manage the API.
3. Choose a specific API, such as Computer Vision API.
4. Link the API to the resource created in step 2.
5. Obtain the unique API Keys and endpoints to access the API.
6. The API endpoints that are leveraged are POST Read and GET Read Result(Explained further)


Prerequisites for the Project.
1. An Azure subscription
2. Node.js
3. Create your Azure subscription, create a Computer Vision resource in the Azure portal to get your key and endpoint. You will need the key and endpoint from the resource you create to connect your application to the Computer Vision service. 
4. Paste the API_KEY in the .env file so that it is not exposed in your server-side code.
5. Endpoints:-
curl -v -X POST "https://eastus.api.cognitive.microsoft.com/vision/v3.2/read/analyze"
curl -v -X GET "https://eastus.api.cognitive.microsoft.com/vision/v3.2/read/analyzeResults/{Operation ID}"

Testing the Application on UI:-
1. Go to the browser. Hit the URL http://64.176.215.214:3000/
2. Enter the image url in the Text Box. Click Submit. Example:- https://i.ytimg.com/vi/tSWCs1TuEZI/maxresdefault.jpg
3. Click on Extract Text.
4. Example images: 
https://i.ytimg.com/vi/tSWCs1TuEZI/maxresdefault.jpg

https://www.southernliving.com/thmb/VqfHkm8AwzyepcL4X_HH0fIaIRA=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/SL-RomanticMessages--5_AlbertEinstein-bcab2e4c4636437c82e6b17bcfef3ef6.jpg

https://www.southernliving.com/thmb/85KWhAViXk-7EsJWYvNBtOXYolI=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/SL-RomanticMessages--4_butterflies-3ae0a1e2abcc45de8301651c7c23af8b.jpg

Testing on Postman:-
1.	Copy the url of the application http://64.176.215.214:3000/in Postman. Select the post request. In headers add Ocp-Apim-Subscription-Key : “your-subscription-key” and Content-Type: “Application/json”. In body, select x-www-form-urlencoded, add image as key and in value – image url. Click on send.
2.	If Image is supported, you will see 200 response. You can get the ID which will required for GET request in ‘action’ inside form in response body.
3.	Change the request type to GET and copy the ID in http://64.176.215.214:3000/:id 
example:- http://64.176.215.214:3000/87f77e9f-5e42-41be-8594-f62259ce537b

How to run the project locally.
1. Create an Computer Vision Azure Resource and get the API_KEY.
2. git clone https://github.com/Pritesh1001/ITIS_6177_Final_Project-main.git
3. npm install
4. paste your API_KEY in .env file.

