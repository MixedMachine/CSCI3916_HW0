# CSCI3916_HW0
 
## Assignment purpose
The purpose of this assignment is to work with Postman become familiar with HTTP, and REST through the testing framework provided by Postman.   

Furthermore, to check in your first node program to github. 

## Assignment goal
You will create a Postman collection and create a REST test within the project. You will need to automate each test and include the required asserts (tests) for each request in the validation.    

## Assignment tasks & requirements
• Create a REST request to get started:     
    – Create an environment variable book_title for the query string for title  
    – Url: https://www.googleapis.com/books/v1/volumes?q={{book_title}} 
    – Use this request to get a JSON response of books with the name Turing in the title.   
    – Parse the result and store the id in a postman variable   
    – Asserts must include  
        ▪ validating books returned have the title turing (e.g. items[i].title)     
        ▪ Response status code (e.g. 200)   
• Create a chained request that requests    
    – Url: https://www.googleapis.com/books/v1/volumes/{{id}}   
    – Using the id you stored from the first request, make sure the second request uses the
    ID pulled from the first request    
    – Create Asserts that:  
        ▪ Validate response contains the ID from the request    
        ▪ Validate response status code (e.g. 200)  
• Modify googlebooks.js     
    – Return an object that contains    
        {   
            data: response.data,    
            status: response.status,    
            statusText: response.statusText,    
            headers: response.headers,  
            requestHeader: response.config.headers  
        }   
    – Review the HTTP Headers in the Request and Response  
    – create text file headers.txt and describe each key value pair in the HTTP header in both request and response and
    check it in     
# POSTMAN TEST
[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/deb2a436a1a1bcfea9cb?action=collection%2Fimport#?env%5BCSC3916_HW0_ENV%5D=W3sia2V5IjoiYm9va190aXRsZSIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImFueSJ9LHsia2V5IjoiaWQiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJhbnkifV0=)
