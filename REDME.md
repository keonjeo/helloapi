# How to start this project

### step1

* rvm install 2.3.1

* rvm gemset create hello_api

* rvm use 2.3.1@hello_api

* gem install bundler

* bundle install


### step2

* rackup -o 0.0.0.0 -p 9292 config.ru



### step3

* brew install httpie

* http get :9292/hello

##### The result: 

<code>
TTP/1.1 200 OK
Connection: Keep-Alive
Content-Length: 28
Content-Type: application/json
Date: Sun, 13 Aug 2017 11:17:43 GMT
Server: WEBrick/1.3.1 (Ruby/2.3.1/2016-04-26)

{
    "message": "Hello  via GET"
}

<code>


* http post :9292/hello


##### The result: 

<code>

HTTP/1.1 201 Created
Connection: Keep-Alive
Content-Length: 29
Content-Type: application/json
Date: Sun, 13 Aug 2017 11:18:03 GMT
Server: WEBrick/1.3.1 (Ruby/2.3.1/2016-04-26)

{
    "message": "Hello  via POST"
}


<code>