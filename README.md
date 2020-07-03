# Execution order of scripts
> In Postman, the script execution order for a single request looks like this:
> A pre-request script associated with a request will execute before the request is sent
> A test script associated with a request will execute after the request is sent workflow for single request

![reqeust-response](req-resp.png)

# demo of test scripts
```js
pm.test("Your test name", function () {
    var jsonData = pm.response.json();    
    pm.environment.set("token", jsonData.token);
    pm.expect(jsonData.id).to.eql(0);
});
```
