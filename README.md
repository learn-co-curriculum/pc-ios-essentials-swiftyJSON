# Using NYC Open Data Using SwiftyJSON

![json](http://dev.bowdenweb.com/js/json/i/hello-my-name-is-json.jpg)

We've said many times before, the internet is essentially a huge database.  Your Facebook photos, the weather history for El Paso, Texas, the headlines for the International Herald Tribune, all of the gyro shops in Istanbul.  Some of those sites, or some organizations, make this data available for developers to build cool things with.

 * Much of the time, these data are returned to you in a format called JSON.  
 * We are going to utilize JSONs from NYC Open Data for our final projects.  
 * JSON probably looks intimidating, but it's essentially a nested hash. Let's call this hash object `response`. 

**Using JSON with Swift.**  Under normal circumstances, "parsing"  a JSON, or searching it for the information that you want, is an ugly process. ON.  SwiftyJSON is a library that makes it easier for us to parse JSON and is straight-forward to implement.  

**Implementing Swifty JSON**
+ Go to [this site.](https://github.com/SwiftyJSON/SwiftyJSON)
+ Create a new Swift file in your project, name is *SwiftyJSON.swift* and paste the SwiftyJSON.swift contents there.
+ In your ViewDidLoad method in your view controller, paste the following code:

```
let filePath = NSBundle.mainBundle().pathForResource("rows", ofType: "json")
        let data =  NSData(contentsOfFile: filePath!)
        let json = JSON(data: data!)
        var actualData = json["data"]        
        
```
In this case *rows* refers to the filename of your JSON.  

And you're good to go!
 
 

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/pc-ios-essentials-swiftyJSON' title='Using NYC Open Data Using SwiftyJSON'>Using NYC Open Data Using SwiftyJSON</a> on Learn.co and start learning to code for free.</p>
