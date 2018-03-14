# Backend General Best Practices

## Monitoring

* Load balancing monitoring
* Per API endpoint response time
* Per server resources monitoring (CPU, RAM, Disk Space, etc…)
* Setup alerts for all previous points
* Use asynchronous logging in code

## Security

* Per API endpoint throttling (mainly login, file uploading, etc…)
* User’s input sanitization
* Do not store plain text password
* Prefer using BCrypt to hash password

## Performance optimization

* Database indexes
* Use of Redis, no read should be done to the database directly
* Use CDN to serve static files
* Use NGinX or Varnish to cache static API requests
* Use Redis to cache dynamix API requests

## Industrialization

* The whole solution should be easy to install and deploy
* Application should support Docker
* API Versionning should be carefully handled
* New versions should be packaged from Continuous Integration
* Each version should be easy to rebuild and redeploy (for emergency fixes or to debug locally)
* Use of GIT
* Database versionning should be handled carefully (applying updates or rollbacking versions should be handled)
* API should be 100% tested with unit tests

## Deploy

* Every deploy should have a changelog
* Documentation
* Swagger up-to-date with meaningfull examples
