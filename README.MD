# Starlette Admin Auth Issue

The code from https://github.com/jowilf/starlette-admin/tree/main/examples/auth 
```shell
uvicorn app:app
```
Although the /admin/ view will resolve endless 303 redirects with Starlette 0.33+ 

Works fine with Starlette 0.32 | starlette-0.32.0.post1
```
pip install -r _working_setup.txt
```
that's ↗ "pip freeze" e.g. with the dependencies of dependencies =) 

* breaks from 0.33: endless redirects
```shell
pip install -r requirements.txt
```

Trying to fix with the pre-release candidate for Starlette Admin, since the same example
works fine when use their code from the repo rather than pip installing starlette-admin
```shell
pip install -r requirements_fix.txt
```
This works!
