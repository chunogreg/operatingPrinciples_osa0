```mermaid
sequenceDiagram

    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa
      Note right of Browser:Browser request HTMl document from server
    Server-->>Browser:  HTml document delivered 
  
   Note right of Browser: The browser uses the javascript to manipulate the DOM and renders the new content
 
