# Session-Management-Research
>Done by: Mahmoud W, Samer, Mahmoud D, Kefah

>8 week research


### What is a session?
A sessions is the unique identification of a user which is sent to the users browser as a cookie or as a GET request. Sessions end when the user closes the browser, or when the web server deletes the session information.

### How are sessions used?
A session is a place to store data. Each user that visits your website has a unique session.  You can use sessions to store and access user data as they browse your application.

### How to manage Sessions?
The main reason of sessions and cookies is the stateless of HTTP. So to maintain state across requests among many other approaches, sessions and cookies is one approach.
### Sessions can be managed by middleware with following options:
* **cookie:** Options object for the session ID cookie. The default value is

```{ path: '/', httpOnly: true, secure: false, maxAge: null }```.
* **genid:** Function to generate the session ID. Default is to use **uuid**
* **name:** The name of the session ID cookie to set in the response (and read from in the request).
* **proxy:** Trust the reverse proxy when setting secure cookies.
* **resave:** If true forces a session to be saved back to store even if it was not modified in the request.
* **rolling:** Forces a cookie to be set on every request.
* **saveUninitialized:** If true it forces a newly created session without any modifications to be saved to the session store.
* **secret:** **It is a required** option and is used for signing the session ID cookie.
* **store:** Session store instance. Default is to use **memory** store.
* **unset:** Controls the handling of session object in the store after it is unset. Either ```delete``` or ```keep``` the session object. Default is to keep the session object.

###### A sipmle example of using the options:
```
var sessionOptions = {
  secret: "secret",
  resave : true,
  saveUninitialized : false
};
```
