# Docker Local Development Proxy

This is a simple proxy for developing local web application UI's and API's at the same time. In order for the proxy to work correctly you need to add the following two lines to your /etc/hosts file



- 127.0.0.1 api.localhost
- 127.0.0.1 web.localhost



To start the proxy simply run `docker-compose up`

Optionally, you can run the above with the `-d` flag to run in the background



After everything is set up you can access your API running on port 8000 and your front end web server running on port 8080 via api.localhost:5000 and web.localhost:5000



NOTE: If you are using Vue's dev server you need to add the following to you vue.config.js file:

`// vue.config.js
module.exports = {
    // options...
    devServer: {
        disableHostCheck: true
    }
}`



## Credits

This is an implementation and customization of Kevin Bradwick's excellent [post](https://dev.to/kevbradwick/how-to-setup-a-reverse-proxy-to-your-host-machine-using-docker-mii) on dev.to