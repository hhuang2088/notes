# Quiz
## Week 2
 
## RSPEC 

XGiven the Triangle class:
	
	class Triangle
	
	  attr_accessor :base, :height
	
	  def initialize(base,height)
	    @base = base
	    @height = height
	  end
	
	  def area
	    0.5 * @base * @height
	  end
	
	end

Write one "describe block" with two "it-blocks"" within. "Before each" test create a triangle with `@base = 4` and `@height = 8`. In the first "it-block" test that the `@base` equals `4` (attribute test). In the second "it-block," test that the `#area` equals `16` (method test).
```
it "initialize base" do
	(triangle.base).should eq(4) 
end


it "calculates area" do
	(triangle.area).should eq(16)
end
```


## Algorithms 
* How can you tell if a method you are looking at is recursive or not?
* - A method is recursive if it calls itself within itself.


__Given the following code__

```
def foo (x)
  puts x
  foo(x - 1) unless x == 0
end

foo 9
```

* What will the screen output of this code be?
* <b>-This will display numbers numbers 9 to 0.</b>
* What is the return value of ```foo 9```
* <b>- This would return nil.</b>



## Iterators
* What would be the output of the following  
* <b>- The output would be the string "Hello, john"</b>

	    def my_func
	        yield "Hello"
	    end
    
    	person = "john"
    	my_func {|greeting| puts "#{greeting}, #{person}" }
    	

* Why does the block have access to the person variable
* <b>-Functions may access any </b>

* Implement each given the following definition:

```
class ArrayContainer
  def initialize(arr)
    @arr = arr
  end
	  
  def each &block
    i = 0
    while 0 < @arr.length
    yield @arr[i]
    i += 1
    end
    @arr
end
```


## HTTP request and response

* Define Server
* -The server is a computer database that holds information and sends information to client side computers.

* Name one thing that goes in a HTTP request headerX
* - 

* Name one thing that could come in an HTTP response bodyX
* -

* Name one status code that could come in an HTTP response headerX
* -

## Intro Sinatra

   * My view is not rendering what I expected it be, twice `params[:my_number]`. What's wrong?
   -It's not displaying the expected output because the data that is stored in the input variable is presumably in the form of an interger. Before it can be displayed it needs to be made into a string. X
 
```
get "/double/:my_number" do
  input = params[:my_number]
  @double = 2*input
        
  erb :show
end
```

## API's 

* What is the difference between JSON and objects in ruby such as ruby hashes or ruby arrays?

Answer: JSON is a string that represents a set of objects.  A ruby hash or array can be represented with a JSON string but the string is not a hash or an array.  A hash is an object that associates keys with values and an array is an object that maintains a list of other objects.


## More Sinatra

* Why is my form not working?X
* 
    
```
<form action="get" method="/">
   <input type="text" name="my_name">
   <input type="submit" value="submit name">
</form>
```

* After the following form is submitted, how would you write code in sinatra to access the params hash and get the ```animal[species]``` value?X
* get "/my_name/params[:species]" do
*   params[:species]
*   end

```
<form action="/animal" method="post" >
   <input type="text" name="animal[species]">
   <input type="text" name="animal[description]">
</form>
```
## HTML/CSS, DOM
Find the 2 errors in this css file:
There shouldn't be a colon after div, and there needs to be a semi-colon seperating two attributes being defined.
	
	div: {
	    color: red
	    float: left
	    }

What's the problem with the following HTML markup?
<b>The id "someID" is being used twice, when it can only be utilized once per html document. </b>

```
<html>
   <head>
      <meta charset="UTF-8">
      <title>Quiz Quiz Quiz</title>
    </head>
	<body>
	   <div id="someId">
	     I'm a Div!
	   </div>
	   <p class="someClass">
	     Lol
	    </p>
	   <h1 class="purple">
	     Blah Blah
	   </h1>
	   <div id="someId">
	     Hello
	   </div>
	            
    </body>
</html>
```

