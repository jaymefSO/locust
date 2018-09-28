`eb open` should open up the locust GUI url which is currently: http://locust-testing.us-east-1.elasticbeanstalk.com/

Locust tests are defined in `locustfile.py` whatever tests are defined there will run when you start the test in the GUI above.  To change tests you edit this file, commit it locally then `eb deploy` to deploy the changes up to EB. 

The tests run against whatever URL is defined in the `TARGET_URL` env var.  Right now it is https://api-stage.cf-fb.org but we may want to change this.  This can be changed using `eb setend TARGET_URL=whatever`
