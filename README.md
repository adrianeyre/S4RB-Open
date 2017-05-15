# S4RB Task - Adrian Eyre #

## Index
* [Task Outline](#Task)
* [User Stories](#Story)
* [Thought Process](#thought)
* [JavaScript with jQuery](#jquery)
* [Ruby with Sinatra](#sinatra)
* [JavaScript with Angular 2](#angular)

## <a name="Task">Task Outline</a>
Imagine you have been tasked by the Account Manager to create a basic reporting application that will allow the account manager to view complaints via a online portal.
The company already has an internal json rest api that stores all the complaints that the business has recieved and the number of corresponding sales in that period.

## <a name="Story">User Stories</a>
```
As an Account Manager
So that I can improve the server to our customers
I would like to view complaint figures
```
```
As an Account Manager
So that I know the complaint figures each month
I would like to view complaint listed monthly
```
```
As an Account Manager
So that I know the complaint figures each quarter
I would like to view complaint listed quarterly
```
```
As an Account Manager
So that I know each month has data
I would like to view month with 0 complaints as 0.00000000
```

## <a name="thought">Thought Process</a>

I have solved this task with three different solutions. The first was using JavaScript and jQuery, the second Ruby with Sinatra the the third with JavaScript and Angular. Each version is fully tests in it retrospective test framework with unit and feature tests. The Angular 2 version was used to experiment with using the framework. I have submitted all three solutions to show different coding qualities in each of the frameworks.

### Steps taken
I started by creating the user stories from the task that was given to me, breaking them down into manageable chunks.

I incorporated the MVC model for both the JavaScript and Ruby versions splitting the dependencies out into classes. Each part of the MVC model is separated into their respective folders so that the code is easily read and maintained.

Good software craftsmanship was used throughout the project such as dependency injecting other classes into the class so that each class had a single purpose.

Tests were put into place before any code was written so that it was clear what was needed to be produced before implementation of code.

### Class Structure
JSONApi

| Class | Description |
|---- | ---- |
| readApi()     | Reads Json object and returns data |

CPMU

| Class | Description |
|---- | ---- |
| calculate    | Calculate CPMU
| quarter      | Calculate quarterly figure
| quartile     | Calculate quartile index
| display_date | Display formatted date
| check_error  | Error checking

## <a name="server">Json Server</a>
### Setup
The internal json rest api can be hosted locally using the following commands:

```shell
$ npm install -g json-server
$ json-server --watch db/db.json

Open http://localhost:3000/CPMU in your web browser
```

## <a name="jquery">JavaScript with jQuery</a>
### Setup
The JavaScript with jQuery can be hosted locally using the following commands:
```shell
$ cd Javascript
```
Running the Jasmine test
```
Open SpecRunner.html in your web browser
```
Running the web application
```
Open index.html in your web browser
```

## <a name="sinatra">Ruby with Sinatra</a>
### Setup
The Ruby with Sinatra can be hosted locally using the following commands:
```shell
$ cd Ruby
$ bundle
$ rvm 2.3.3
```
Running the Rspec test
```
$ rspec
```
Running the web application
```
$ ruby ./app/controller.rb
Open http://localhost:4567 in your web browser
```

## <a name="angular">JavaScript with Angular 2</a>
The JavaScript with Angular 2 can be hosted locally using the following commands:
```shell
$ cd Angular
```
Running the web application
```
Open index.html in your web browser
```



![Example Reporting Porta](/example-2.png "Example Reporting Portal")

