```mermaid
    sequenceDiagram
    
        Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
        Note right of Browser:form submission
        Server-->>Browser:  redirection request, server tells browser to make new HTTP GET request to the location as stated in the location header
    
         Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
       Server-->>Browser:  Note page reloaded 
       Note right of Browser: Reloading notes page triggers off three other request from Browser
         Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
         Note right of Browser: Browser requests css file
      Server-->>Browser: server returns the css file
    
     Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
     Note right of Browser: Browser requests javascript file
      Server-->>Browser: server returns the javascript file
     Note right of Browser: Browser executes the code and discovered there was a JSON file needed
