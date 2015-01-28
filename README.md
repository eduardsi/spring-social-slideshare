# spring-social-slideshare

Spring Social provider module for [SlideShare API](http://www.slideshare.net/developers).


# Project Status

Currently, only `SlideshowTemplate`(slideshow related operations) is implemented.  
If you need other operations(user, leads, campaign, etc) or implementation of Spring Social's _Service Provider 
Connect Framework_ (such as `ApiAdapter`, `ConnectionFactory`, `ServiceProvider`, etc), please ping me or [create an 
issue on github](https://github.com/ttddyy/spring-social-slideshare/issues). 
I will implement them if there is a need.

I'm [@ttddyy](https://twitter.com/ttddyy) on twitter if you want to ping me. :)   


## key features

- `SlideshowTemplate` to interact with SlideShare slideshow related operations in java 


## library versions

| spring-social-slideshare | spring-io-platform |                                                 note |
| ------------------------:| ------------------:|------------------------------------------------------| 
|             1.0.0, 1.0.1 |      1.1.1.RELEASE | works with `spring-io-1.1.0` or `spring-4.1.2` above |

* `spring-io-platform-1.1.1` comes with `spring-social-1.1.0` and `spring-framework-4.1.4`.

* [Changelog](CHANGELOG.md)

## how to get


```xml
  <dependency>
      <groupId>net.ttddyy</groupId>
      <artifactId>spring-social-slideshare</artifactId>
      <version>1.0.1</version>
  </dependency>
```

# Usage

```java
  SlideShare slideShare = new SlideShareTemplate("api_key", "shared_secret");
  SlideshowOperations slideshowOperations = slideShare.slideshowOperations();

  // you can do: get/search/edit/delete/upload slideshows
  Slideshow slideshow = slideshowOperations.getSlideshow("0123456", ...);
```

# Demo Code

I wrote a demo project: [spring-social-slideshare-demo](https://github.com/ttddyy/spring-social-slideshare-demo).

The demo covers basic usecases (get/search/upload/edit/delete slideshow), and simply written in 
[Application.java](https://github.com/ttddyy/spring-social-slideshare-demo/blob/master/src/main/java/demo/Application.java). 

