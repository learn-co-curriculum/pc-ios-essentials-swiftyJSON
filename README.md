# Using NYC Open Data Using SwiftyJSON

![json](http://dev.bowdenweb.com/js/json/i/hello-my-name-is-json.jpg)

 * We've said many times before, the internet is essentially a huge database.  Your Facebook photos, the weather history for El Paso, Texas, the headlines for the International Herald Tribune, all of the gyro shops in Istanbul.  Some of those sites, or some organizations, make this data available for developers to build cool things with.
 * Much of the time, these data are returned to you in a format called JSON.  
 * We are going to utilize JSONs from NYC Open Data for our final projects.  
 * JSONs probably looks intimidating, but it's essentially a nested hash. Let's call this hash object `response`. 
  * If you see a bunch of indecipherable bunched up text, download this [JSON chrome extension](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=en) to save your eyes.
  
* Using JSON with Swift.  Under normal circumstances, "parsing"  a JSON, or searching it for the information that you want, is an ugly process.  Enter a library called SwiftyJSON.  SwiftyJSON is a library that is easy to implement that makes it easier for us to parse JSON.  
* Implementing Swifty JSON
+ Go to [this site.](https://github.com/SwiftyJSON/SwiftyJSON)
+ Create a new Swift file in your project, name is *SwiftyJSON.swift* and paste the SwiftyJSON.swift contents there.
+ In your ViewDidLoad method in your view controller, paste the following code:

```
let filePath = NSBundle.mainBundle().pathForResource("rows", ofType: "json")
        let data =  NSData(contentsOfFile: filePath!)
        //print(data)
        let json = JSON(data: data!)
        var actualData = json["data"]
        
        
```
And you're good to go!
 
 
