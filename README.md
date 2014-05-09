My Ruby and RoR code conventions
================================

My Ruby and RoR code cenventions - nothing very new but handy to have them here.

@@ WIP

Basic principles
----------------

* DRY - Don't Repeat Yourself
* Convention over Configuration

Source code style
-----------------

* two spaces, no tabs
* width 120 

Spelling
--------

* Names are important - think hard to find good names 
* everything is spelled in English

###Methods 

Methods are always written in Snake Case

    def kenny_was_killed_by_accident
      puts "R.I.P"
    end
    
If a method should answer a question with a boolean, add a question mark

    def was_kenny_killed_by_accident?
      true
    end
    
Tell where the method received it's return values

    def parameters_from_request
      params
    end

Add parentheses, if the method receives parameters

    def filter_params(params)
      # do something
    end

Ommit parentheses, if no parameters are expected

    def calculate_seconds_from_time
      # calculate
    end
    
###Classes and Modules

Have to be written in camel case by Ruby requirement

    module PreFormatter
      class ForJson
        
      end
    end
    
###Constants

Write them always in uppercase letters seperated by an underscore

    RUBY_IS_REALLY_AWESOME = true
    
Hash
----

Use curly braces and the 1.9 convention for key - value assignments

    user = {
      first_name: 'Andy',
      last_name: 'Wenk'
    }
    
Blocks
------

Always use the `do` - `end` for multiline blocks

    user.each do | k, v |
      combined = "#{k}:#{v}"
      puts combined
    end
    
Always use curly braces for one liners

    user.each { | v | puts v }

Conditionals
------------

Try to write english sentences

    is_even = true if number % 2 == 0
    
Use unless instead of if

    if !is_even
      # do something
    end
    
    unless is_even
      # do something
    end

Various
-------

* use &&, || instead of and, or
* don't use `for` ... `in`



