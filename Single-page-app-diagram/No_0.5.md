```mermaid
sequenceDiagram

    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
      Note right of Browser:form submission
    Server-->>Browser:  server tells browser to make new HTTP GET request 
  
   Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
   Server-->>Browser:  Note page reloaded 
   Note right of Browser: Reloading notes page triggers off three other request from Browser
