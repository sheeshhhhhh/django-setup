# django-setup

### terms
- **root**- eto yung pinaka taas ng project mo na dapat pag nag "dir" or "ls" ka na command is kita dapat yung requirements.txt
+ **< port >** - etong port na nakalagay sa run server is optional ibig sabihin lang neto is kahit wala kang ilagay ok lang
+ **launch.json** - eto yung file na ipoprovide sayo if ever man na nasa marscode ka kugn wala edi wala lang to

## FOR WHAT REASON?
This is our project for sir marjon where we need to create a Point of sale System made with django with no database but rather just array in the view

## FEATURES
- [X] to Check add X (wala tong silbi sa code sa readme lang)
- [ ] Add Product
- [ ] Edit Product
- [ ] The Point of Sale
- [ ] Search in the POS main
- [ ] History
- [ ] VAT tax (12%)
- [ ] Dashboard
- [ ] Login and Signup Authentication (Sa huli na to kapag ayos na lahat hinde naman masyadong required) 
- [ ] Print of Receipt

## TO RUN AND INITIALIZE

# linux
root (look in the terms para malaman mo meaning)
```sh
    python3 -m venv venv

    #to activate
    source venv/bin/activate
```

# Windows
root (look in the terms para malaman mo meaning)
```powershell
    python -m venv venv
    .\venv\Scripts\activate
```

# install required Dependencies 
root (look in the terms para malaman mo meaning)
```powershell   
    pip install -r requirements.txt
```

# to start
```powershell
    cd .\pos\
    python manage.py runserver <port>
```

# NOTES
if you are in mars code you need to have 
in settings.py
```python
    CSRF_TRUSTED_ORIGINS = [
        # for origin and csrf_token in the forms ilagay mo lang url na binigay ng marscode
        # example
        'https://ftvd7g7t-04u2tkb8-ok58ctvccia8.ac4-preview.marscode.dev'
    ]
    ALLOWED_HOSTS = [
        # dito din website name lang
        # name of the website with https
        "https://ftvd7g7t-04u2tkb8-ok58ctvccia8.ac4-preview.marscode.dev", 
        # with no https
        "ftvd7g7t-04u2tkb8-ok58ctvccia8.ac4-preview.marscode.dev"
    ]
```

in `launch.json` that marscode will provide in order to run just paste this 
```json
    // launch.json is for marscode 
    {
      "version": "0.0.1",
      "configurations": [
        {
          "name": "Start Application",
          "type": "debugpy",
          "request": "launch",
          "program": "pos/manage.py",
          "args": [
              "runserver",
              "0.0.0.0:8080"
          ],
          "console": "internalConsole",
          "justMyCode": true
      }
      ]
    }
``` 