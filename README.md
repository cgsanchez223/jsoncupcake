Unit 28.2 - External API Requests in Flask
- This chapter is very informative with learning how to connect an external API to your project.

- Python Requests
    - (venv) $ pip install requests
    - To activate in file use:
        - import requests
        - resp = requests.get(
            "https://itunes.apple.com/search",
            params={"term": "billy bragg", "limit": 3}
        )
- Many API do require a secret key to use in order to protect information. It is necessary to hide this password
    - In a file you can identify the key
        - API_SECRET_KEY = "jdfghfkgdg9345dkjfgdfg"
        - from secrets import API_SECRET_KEY
        - add secrets.py to the .gitignore

________________________________________________________________________
Unit 28.3 - REST and JSON APIs
- RESTful APIs
    - Client-server model, statelessness and cacheability
    - Usually have a base url and a resource
    - Use GET, POST, PUT, DELETE
    - Use structured routes
- RESTFUL APIs with Flask
    - Respond with JSON
    - Can use jsonify
    - Can receive data with request.json
__________________________________________________________________________
- Assignment - Cupcakes
    - Purpose of the assignment is to create a CRUD application where you can also view the API and JSON of the model data
    - Cucpcake model contains id, flavor, size, rating, and image
    - Routes include:
        - GET /api/cupcakes - Get information about cupcakes, responds with JSON data
        - GET /api/cupcakes/[cupcake-id] - Get data about a single cupcake, responsds with JSON data
        - POST /api/cupcakes - Creates a cupcake. Responds with JSON data.
        - PATCH /api/cupcakes/[cupcake-id] - Updates information on cupcake
        - DELETE /api/cupcakes/[cupcake-id] - Deletes information
        - GET '/' - home page