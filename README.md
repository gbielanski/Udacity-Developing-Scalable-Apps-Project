App Engine application for the Udacity training course.

## Products
- [App Engine][1]

## Language
- [Python][2]

## APIs
- [Google Cloud Endpoints][3]

## Setup Instructions
1. Update the value of `application` in `app.yaml` to the app ID you
   have registered in the App Engine admin console and would like to use to host
   your instance of this sample.
1. Update the values at the top of `settings.py` to
   reflect the respective client IDs you have registered in the
   [Developer Console][4].
1. Update the value of CLIENT_ID in `static/js/app.js` to the Web client ID
1. (Optional) Mark the configuration files as unchanged as follows:
   `$ git update-index --assume-unchanged app.yaml settings.py static/js/app.js`
1. Run the app with the devserver using `dev_appserver.py DIR`, and ensure it's running by visiting your local server's address (by default [localhost:8080][5].)
1. (Optional) Generate your client library(ies) with [the endpoints tool][6].
1. Deploy your application.

## Task1: Add Sessions to a Conference - design explaination
Session Datastore entity has all String properties except duration (IntegerProperty) and date (DateProperty). 
I designed speaker as String because it is the simplest solution and meets the requirements. It can be easily extended for further purpose if needed.
The duration propertied is Integer because it can be represented by number of minutes.
The field typeOfSession is string because it is enumeration in SessionForm and it is easy to convert in the same way as in Profile is teeShirtSize field.
The start is string because it is the easiest in use and meet the requirement that it should be ordered.
The fields date is Date and highlights is String because it seems natural choice. 

[1]: https://developers.google.com/appengine
[2]: http://python.org
[3]: https://developers.google.com/appengine/docs/python/endpoints/
[4]: https://console.developers.google.com/
[5]: https://localhost:8080/
[6]: https://developers.google.com/appengine/docs/python/endpoints/endpoints_tool
