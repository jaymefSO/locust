`eb open` should open up the locust GUI url which is currently: http://locust-testing.us-east-1.elasticbeanstalk.com/

Locust tests are defined in the `locustfile.py` file.  Whatever tests are defined there will run when you start the test in the GUI above.  To change tests you edit this file, commit it locally then `eb deploy` to deploy the changes up to EB. 

The tests run against whatever URL is defined in the `TARGET_URL` env var.  Right now it is pointed at https://api-stage.cf-fb.org

The EB Environment is running in US region and is on a large instance so it should have plenty of resources to simulate heaving testing. 
