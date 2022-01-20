# Cedric's Notes for code-301n24 course

## CRUD

### Status Codes Based On REST Methods

In your own words, describe what each group of status code represents:

100’s = These are informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.


200’s = These are the success codes. They tell the client that its request was accepted. In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.


300’s = These are redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore. This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location.


400’s = These are the client error codes. They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication, etc. A client is sending incorrect input and should confirm the input parameters are correct before retrying the request.



500’s = These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server. These errors can be temporary or permanent. Usually it’s best for the client to retry the same request.


What is a status code 202?
Accepted response status code indicates that the request has been accepted for processing, but the processing has not been completed; in fact, processing may not have started yet.

What is a status code 308?
Permanent Redirect redirect status response code indicates that the resource requested has been definitively moved to the URL given by the Location headers.

What code would you use if an update didn’t return data to a client?
What code would you use if a resource used to exist but no longer does?
What is the ‘Forbidden’ status code?

#### Videos

Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes

Why do we need to pull our MongoDB database string out of our server and put it into our .env?

What is middleware?

What does app.use(express.json()) do?

What does the /:id mean in a route?

What is the difference between PUT and PATCH?

How do you make a default value in a schema?

What does a 500 error status code mean?

What is the difference between a status 200 and a status 201?


## Things I want to know more about
