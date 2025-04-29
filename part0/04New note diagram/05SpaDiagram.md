```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET /main.css
    activate server
    server-->>browser: CSS file
    deactivate server

    browser->>server: GET /spa.js
    activate server
    server-->>browser: JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code

    browser->>server: GET the data json 
    activate server
    server-->>browser: [{ "content": "Desmo13 in yt", "date": "2003-14-2" }, ... ]
    deactivate server

    Note right of browser: The browser renders the notes dynamically without reloading the page
    ```
