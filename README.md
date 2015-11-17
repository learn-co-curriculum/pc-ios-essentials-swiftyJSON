# Using NYC Open Data Using swiftyJSON


 * JSON is a "data-interchange format" which is basically a neat way to look at the responses from an APIs
  * If you see a bunch of indecipherable bunched up text, download this [JSON chrome extension](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=en) to save your eyes.
  * This thing probably looks intimidating, but it's essentially a nested hash. Let's call this hash object `response`. 
  * If we want to pull the `data` array out of this hash that would be `response["data"]`
  * Drill down deeper to the first item in that array: `response["data"][0]`. 
  * If we wanted to pull the url for that first image in the array:
```
response["data"][0]["images"]["original"]["url"] #=> "http://media0.giphy.com/media/FiGiRei2ICzzG/giphy.gif"

```

``` let filePath = NSBundle.mainBundle().pathForResource("rows", ofType: "json")
        let data =  NSData(contentsOfFile: filePath!)
        //print(data)
        let json = JSON(data: data!)
        var actualData = json["data"]
        
        
```


 
 
