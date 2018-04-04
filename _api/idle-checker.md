---
title: '!idlechecker'
position: 1
type:
description: >-
  Controls aspects of the Idle Checker / Idle Mover functionality. When enabled,
  users who are idle longer than the designated time threshold will be
  automatically moved to the specified channel.
parameters:
  - name: action
    content: '"enable" or "disable"'
  - name: limit
    content: Limit the number of books returned
content_markdown: >-
  This call will return a maximum of 100 books

  {: .info}


  Lists all the photos you have access to. You can paginate by using the
  parameters listed above.
left_code_blocks:
  - code_block: >-
      $.get("http://api.myapp.com/books/", { "token": "YOUR_APP_KEY"},
      function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.myapp.com/books/", token="YOUR_APP_KEY")
      print r.text
    title: Python
    language: python
  - code_block: >-
      var request = require("request");

      request("http://api.myapp.com/books?token=YOUR_APP_KEY", function (error,
      response, body) {

      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: 'curl http://sampleapi.readme.com/orders?key=YOUR_APP_KEY'
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
          "id": 1,
          "title": "The Hunger Games",
          "score": 4.5,
          "dateAdded": "12/12/2013"
        },
        {
          "id": 1,
          "title": "The Hunger Games",
          "score": 4.7,
          "dateAdded": "15/12/2013"
        },
      ]
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid offset"
      }
    title: Error
    language: json
---