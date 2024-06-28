sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes/new_note
    activate server
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: Tells the server that data is JSON. Content-Type header is application/JSON.
    Note right of server: No redirect this time.
