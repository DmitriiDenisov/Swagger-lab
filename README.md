# Swagger-lab

### Instructions: 

1. Copy files from [this](https://github.com/sanjan/flask_swagger) repo
Structure of your project now should be:
```
.
├── static
│   ├── css
│   │   └── swagger-ui.css
│   ├── img
│   │   ├── favicon-16x16.png
│   │   └── favicon-32x32.png
│   └── js
│       ├── swagger-ui-bundle.js
│       ├── swagger-ui-standalone-preset.js
│       └── swagger-ui.js
└── templates
    ├── swaggerui.html
```

2. Write your API spec for Swagger. Go to [Swagger Editor](https://editor.swagger.io/) and write your API spec in YAML. 

3. Once you are ready go to File->Convert and save as JSON. Example of such [json](https://github.com/sanjan/flask_swagger/blob/master/static/hello_api.json). Also Swagger Editor itself by default gives you a great example

4. Return swaggerui.html with flask render_template in your preferred route, example:
```
@app.route('/api/docs')
def get_docs():
    print('sending docs')
    return render_template('swaggerui.html')
```

[Source](https://dev.to/sanjan/how-to-add-swagger-ui-to-a-plain-flask-api-project-with-an-openapi-specification-file-1jl8)


## Hints:

If you change your json config file but don't see any change in Swagger then hold down the Shift button and click the Reload button (because browsers cache some files, this will force it to update config file)
