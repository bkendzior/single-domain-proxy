This project runs a very simple reverse-proxy that will mimic akamai or another
caching service setting a moovweb subdomain project as the origin for an
existing www. project. 

1. Host hack your intended single-domain to point to the nginx server we're about to run
  - 127.0.0.1 digikeytest.digikey.com

2. Host hack your intended moov-origin, skip this step if client has already set up CNAMES
  - 54.208.112.58 moov-origin-stage.digikeytest.digikey.com

3. Install nginx
  - brew install nginx

4. Clone this project locally

5. Edit nginx.conf to send requests going to your single domain to use the moovweb origin

6. Run nginx using the included nginx.conf as your configuration file
  - $nginx -c '~/path/to/this/folder/nginx.conf'
