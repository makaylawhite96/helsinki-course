sequenceDiagram
participant browser
participant server


    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Note right of browser: Sends JSON data using the input value as the content and the current time stamp as the date 
    activate server
    server-->>browser: 201 Response (Successfully created and added to notes list)
    deactivate server
    Note left of server: preventDefault() is used to prevent another GET request (page reload)