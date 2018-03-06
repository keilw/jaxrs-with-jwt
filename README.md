# Using the sample project

If you want to play around with the example, please follow hese steps

    Get the maven project and build it (same old maven clean install)
    Deploy on a Java EE 7 container
    Tweak your server security options to protect it using a realm named file and ensure that you include the members under the users group. Both these constraints are dictated by the web.xml descriptor (see above) – you can also choose to modify it as per your choice. Here is a snapshot from the Payara server

test-jwt-snippet-3

    Issue a HTTP GET to http://localhost:8080/jaxrs-with-jwt/auth/token
    Copy the token in the HTTP response header (jwt)

test-jwt-snippet-1

    Issue a GET request to http://localhost:8080/jaxrs-with-jwt/resources/books and include the JWT in the HTTP Authorization header (prepend it with Bearer)
