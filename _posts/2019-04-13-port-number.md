Developing web app using Flask requires port assignment. When we close the app and run it again on terminal, it won't show up because the "Address is already in use." If this happens, we can have a workaround by killing the port number associated to the app. 

To kill the port number associated to the app, first we check the look for it:

```
$ lsof -i :8000
```

Once we find the port number, we can now delete it:

```
kill -9 xxxxx
```

As simple as that.