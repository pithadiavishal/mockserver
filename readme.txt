Step 1:
set env variable
MOCKSERVER_INITIALIZATION_JSON_PATH="D:\mockserver\mocks\health.json" (absolute path of the json)
Step 2:
run the command to start the mock server
java -jar mockserver-netty-5.14.0-shaded.jar -serverPort 1080
Step 3:
check mockserver dashboard
http://localhost:1080/mockserver/dashboard
step 4:
check initialization api
http://localhost:1080/health
step 5:
run the command to set expectation in the mockserver
curl -X PUT "http://localhost:1080/mockserver/expectation" -d @"mocks/test.json"
