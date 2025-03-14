# Part-0.4,0.5,0.6-Sequence-Diagram
```mermaid
sequenceDiagram
  participant browser
  participant server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server->>browser:HTML document
  deactivate server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server->>browser: the css file
  deactivate server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
  activate server
  server->>browser: the js file
  deactivate server
  
  Note right of browser:Browser starts executing the javascript code that fetches the JSON from the server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server->>browser: content[{"content":HTML is easy but JS is hard","date":"2025-3-12"},...]
  deactivate server
```
```mermaid
sequenceDiagram
  participant User
  participant browser
  participant server

  User->>browser:GET https://studies.cs.helsinki.fi/exampleapp/spa
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server->>browser :https://studies.cs.helsinki.fi/exampleapp/spa
  browser->>User:https://studies.cs.helsinki.fi/exampleapp/spa
  deactivate server


