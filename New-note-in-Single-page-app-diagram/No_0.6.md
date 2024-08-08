```mermaid
sequenceDiagram

    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
      Note right of Browser:Browser sends only one POST request
  Server-->>Browser:  server responds to the request
   Note left of Server: Server responds with code 201 created
  
 
