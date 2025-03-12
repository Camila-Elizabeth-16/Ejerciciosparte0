```mermaid
sequenceDiagram
    participant browser
    participant server
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of browser: El controlador de eventos crea una nueva nota, la agrega a la lista de notas, renderiza la lista de notas en la página y envía la nueva nota al servidor.
    server-->>browser: HTTP201 new_notes_spa.json {"message":"note created"}
    deactivate server
  
