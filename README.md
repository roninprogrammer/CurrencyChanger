# CurrencyExchange

Design a page with an input field and a button. The input field is currency and the button to call the api.
 
 Call this api 
 
 <b>GET</b>
 https://exchangeratesapi.io/api/latest?base=MYR
 
 which base=???
 
 Is your input field value. If not enough time, can just hardcode to MYR.
 Display the api result as a list, with Currency and Rate as header.
 
 For example,
 
 | Currency | Rate        |
 |----------|-------------|
 | AUD      | 0.3346779357 |


<b>Best easier way for consuming a REST api on Android</b>
1) There always was one nagging issue in the back of our minds: speed. There are times when the app isn’t as snappy as we’d like it to be. After some profiling, benchmarks, and common sense, we determined that retrieving data from the API (the networking) was the bottleneck.

2) Let's look at back , SimpleHttpClient is an implementation to do HTTP requests, But you will have to handle everything manually like parsing the response and so many. It runs on whichever thread you are calling it from. To run it in a separate thread you will have to create an AsyncTask to retrieve data from Canvas’ servers. no orientation-change support, no ability to cancel network calls, as well as no easy way to make API calls in parallel. With the exception of Froyo and Gingerbread, AsyncTasks (by default) run in a serialized fashion. In a practical sense, this means that only one AsyncTask is running at any given time. Views that require multiple API calls (the DashBoard currently has 7) run extremely slow; sometimes taking multiple seconds to load.

3) Luckily, there are a few third party libraries that provide support for concurrent background threads, network caching, as well as other features that clean up networking code substantially. Volley and Retrofit library was created to make the HTTP request very simple by reducing boilerplate code. Using this you have to write only a few lines of codes to make an HTTP request and the HTTP requests will be pushed to separate thread automatically.

![alt text](http://i.imgur.com/tIdZkl3.png "")


If also if your using SimpleHttpClient and AsyncTask are written in 30lines of code, you can achieve the same using Retrofit or volley in within 6 to 8 lines of code. 

So, retrofit is winrar and most easier way for consuming a REST api on Android

