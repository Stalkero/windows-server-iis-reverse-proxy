# How to fix Windows Server Reverse Proxy
If you like me have an issue when you create your reverse proxy to your service and you get 500 error. Here's how to fix it


## Add server variables 

Go to URL Rewrite module of your Reverse Proxy website

And on the right menu bar find `View server variables`

Create two variables:

-`HTTP_ACCEPT_ENCODING`
-`HTTP_X_ORIGINAL_ACCEPT_ENCODING`

## Edit your reverse proxy inbound role

In server variables add in `Server variable name` variable `HTTP_X_ORIGINAL_ACCEPT_ENCODING`

Set it to value `HTTP_ACCEPT_ENCODING`

Add it 


Crate second variable with name `HTTP_ACCEPT_ENCODING`

And set its vaule to something random for ex. `eee`
