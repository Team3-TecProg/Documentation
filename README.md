
# STYLE SHEET

In this document you will see how to program using pre set technics about the code, organization of files and more.

* [1. Header](#1-header)
* [2. Identation and spacing](#2-indentation-and-spacing)
* [3. Syntax](#3-syntax)
* [4. Naming](#4-naming)
* [5. Comments](#5-comments)
* [6. Classes and modules](#6-classes-and-modules)
* [7. Exceptions](#7-exceptions)
* [8. Collections](#8-collections)
* [9. References](#9-references)

# 1. Header

* The header must content the **class name**, **file name** and **description** of the class. The lines of `#` contains 70 `#`.

```Ruby
######################################################################
# Class name: CommentsController
# File name: comments_controller.rb
# Description: Controller used to communicate with the view highways/show
######################################################################
```

# 2. Indentation and Spacing

* Indentations levels are defined with a hard tab, which size is of four Spacings.

```Ruby

#right
def enterprise_group_ranking
    @quantity = params[:sanctions_count]
    @enterprises = Enterprise.where(sanctions_count: @quantity).paginate(:page => params[:page], :per_page => 10)
end
```
* There are only one statement per line.

```Ruby
# wrong
puts 'testcase'; # superfluous semicolon

puts 'test'; puts 'case' # two expressions on the same line

#right
puts 'testcase'

puts 'test'
puts 'case'
```

* Classes with no body definitions are not defined in a single-line format.

```Ruby
#wrong
PaymentClass = Class.new(Payment)

#right
class Payment < ActiveRecord::Base
    #content starts here
end
```

* Methods also must not be defined in a single-line format.

```Ruby
#wrong
def refresh!; something; something_else; end

#right
def refresh!
    s = SanctionType.find_by_description(self.description)
end
```

* Spaces are used after:
  * commas
  * colons
  * operators
  * semicolons
  * around {, [, ( and before }, ] and )
  * Spaces are also used before operators.
  * The exception regarding operators is the exponent operator.
  * No spaces are used after `!`.

```Ruby
#wrong
array = [element1,element2,element3]

puts "(I'm a string)"
puts "[I'm a string]"
puts "{I'm a string}"

range1 = ( 1 .. 10 )

exponent_variable = 2 ** 5

false_boolean = ! true

#right
array = [ element1, element2, element3 ]

puts "( I'm a word )"
puts "[ I'm a string ]"
puts "{ I'm a string }"

range1 = (1..10)

exponent_variable = 2**5

false_boolean = !true
```

* No spaces are used inside range operators.
* The **when** statement is indented one level deeper than **case** statement.

```Ruby
#wrong
case
when variable.action == ''
  puts 'Case 1'
when variable.action == 'variable_action'
  puts 'Case 2'
when variable.action == 'wrong_variable_action'
  puts 'Case 3'
else
  variable.action
end

#right
case
when variable.action == ''
        puts 'Case 1'
    when variable.action == 'variable_action'
        puts 'Case 2'
    when variable.action == 'wrong_variable.action'
        puts 'Case 3'
    else
        variable.action
end
```

* Methods are separated between them with empty lines. There are no empty lines between the method definition and its scope.

```Ruby
#wrong
def enterprise_group_ranking

  @quantity = params[:sanctions_count]
  @enterprises = Enterprise.where(sanctions_count: @quantity).paginate(:page => params[:page], :per_page => 10)

end
def payment_group_ranking

  @quantity = params[:payments_count]
  @enterprises = Enterprise.where(payments_count: @quantity).paginate(:page => params[:page], :per_page => 10)

end

#right
def enterprise_group_ranking
    @quantity = params[:sanctions_count]
    @enterprises = Enterprise.where(sanctions_count: @quantity).paginate(:page => params[:page], :per_page => 10)
end

def payment_group_ranking
    @quantity = params[:payments_count]
    @enterprises = Enterprise.where(payments_count: @quantity).paginate(:page => params[:page], :per_page => 10)
end
```

* Parameters of method calls, when spamming more than one line, are indented.

> Pode ter parentesis nos métodos? Acho que não.

```Ruby
#wrong
def a_simple_method ( argument_one, argument_two, argument_three, argument_four,argument_five, argument_six, argument_seven)
    #content starts here
end

#right
def a_simple_method ( argument_one,
                      argument_two,
                      argument_three,
                      argument_four,
                      argument_five,
                      argument_six,
                      argument_seven )
    #content starts here
end
```

* Each line is limited to 80 characters.

```Ruby
#wrong
long_variable = "here_have_a_very_long_string_to_exemplify_a_line_thats_have_more_than_80_characters."

#right
long_variable = "here_have_a_very_long_string_to_exemplify_a_line_thats_have_80_characters."
```

* Align the element of an array that appears in more than one line.

```Ruby
#wrong
a_long_array = [ element1, element2, element3, element4, element5, element6,
element7, element8, element9, element10, element11 ]

#right
a_long_array = [ element1, element2, element3, element4, element5, element6,
                 element7, element8, element9, element10, element11 ]

```

# 3. Syntax

* Every variable must be initialized.

```Ruby
#wrong
user_name
user_age

#right
user_name = ""
user_age = 0

```

* `::` is used only for constants and constructors. Not for regular method invocation.

```Ruby
#wrong
PaymentClass::payment_class_method

#right
PaymentClass.payment_class_method
EnterpriseModule::EnterpriseSomeClass::SOME_CONST
```
* Optional parameters are defined at the end of the parameters list.

* `each` must be used instead of `for`, unless it is unavoidable.


```Ruby
#wrong
def last_sanction
    sanctions = [ "section1","section2","section3" ]

    for sanction in sanctions
        puts sanction
    end
end

#right
def last_sanction
    sanctions = [ "section1","section2","section3" ]

    sanctions.each do |sanction|
        puts sanction
    end
end
```

* Use `if`/`else` statement to express conditions. The condition of a `if`/`else` statement is written on the same line and between parenthesis, and the body of an `if`/`else` statement is closed by `{}`. Opening braces are written on the same line.

```Ruby
#wrong
if 5 > 4
    puts "It's true"
end

#right
if ( 5 > 4 )
    puts "It's true"
end
```

* Every `if` statement must have an additional `else` statement.

```Ruby
#wrong
user_name = "Bob"

if(user_name != nil)
    puts user_name
end

#right
if( user_name != nil )
    puts user_name}
else
    #nothing to do
end
```

* Only one expression per line is used in the body of a constructor, like `if`/`else`.
[comment]: # (* The nested form `if` x;... must not be used.)
* Ternary Operator ?: must not be used. `if`/`then`/`else`/`end` must be used instead.
* The operator `!` must be used instead of `not`.
* The operators `&&` and `||` must not be used. Instead, are used the keywords `and` and `or`.

```Ruby
#wrong
if ( 5 > 4 && 6 > 5 )
    puts "It's true"
end

if ( 5 > 4 || 6 > 5 )
    puts "It's true"
end

#right

if ( 5 > 4 and 6 > 5 )
    puts "It's true"
end

if ( 5 > 4 or 6 > 5 )
    puts "It's true"
end
```

* `unless` must not be used with `else`. `if` must be used instead.

* Parenthesis around parameters of methods that are part of an internal DSL, such as Rake, Rails or RSpec, methods that have a keyword status in Ruby, like attr_reader or puts, and attribute access methods, must be omitted. In any other methods, parenthesis must be used around parameters.

```Ruby
#wrong
class Payment
    attr_reader( :name, :date )
    # content starts here
end

#right
class Payment
    attr_reader :value, :date
    # content starts here
end
```

# 4. Naming

* Names are defined in **english**.
* snake_case is used for:
  * symbols
  * methods
  * variables
  * naming files
  * naming directories

```Ruby
  #wrong
def LastPayment
    puts paymentVariable
end

#right
def last_payment
    puts payment_variable
end
```

```Ruby
#wrong
sanctioType.rb
#right
sanction_type.rb
```

```Ruby
#wrong
App/allModels/sanction_type.rb

#right
app/all_models/sanction_type.rb
```
* camelCase is used for classes.

```Ruby

#wrong
class User_controller < ActiveRecord::Base
    #class content
end

#right
class UserController < ActiveRecord::Base
    #class content
end

```

* SCREAMING_SNAKE_CASE is used for constants and global variables.

```Ruby
#wrong
constant_sanction = "I'm a constant"

#right
CONSTANT_SANCTION = "I'm a constant"
```

# 5. Comments
* Use block comments instead of single line comments.

```Ruby
#wrong
=begin
comment line
another comment line
=end

#right
# good
# Comment line.
# Another comment line.
```

* Comments are written in english.
* Comments longer than one word are Capitalized, and end with a period. A space is used after a period.

```Ruby
#wrong

# i'm a long comment, you should've notice that my lenght is being
# greater quickly

#right

# I'm a long comment, you should've notice that my lenght is being
# Greater quickly.
```

[comment]: # (Comment Annotations)


# 6. Classes and Modules

* Classes must have a consistent structure. The class definition is followed by, in this order: `extend`and `include`, inner classes, constants, attribute macros, other macros (if any), public class methods, initializations, public instance methods, and, near the end, protected and private methods.

```Ruby
class Payment
    # extend and include go first
    extend SomeModule
    include AnotherModule

    # inner classes
    CustomErrorKlass = Class.new(StandardError)

    # constants are next
    SOME_CONSTANT = 20

    # afterwards we have attribute macros
    attr_reader :name

    # followed by other macros (if any)
    validates :name

    # public class methods are next in line
    def self.some_method
        #content starts here
    end

    # initialization goes between class methods and other instance methods
    def initialize
        #content starts here
    end

    # followed by other public instance methods
    def some_method
        #content starts here
    end

    # protected and private methods are grouped near the end
    protected

    def some_protected_method
        #content starts here
    end

    private

    def some_private_method
        #content starts here
    end

end
```

* Multi-line classes must not be nested. Instead, each class must have its own file.

```Ruby
# wrong

# foo.rb
class User
    class Payment
        # 30 methods inside
    end

    class State
        # 20 methods inside
    end
  # 30 methods inside
end

# right

# foo.rb
class User
    # 30 methods inside
end

# foo/bar.rb
class User
    class Payment
        # 30 methods inside
    end
end

# foo/car.rb
class User
    class State
        # 20 methods inside
    end
end

```

* Modules should be preferred instead of classes, if they only have class methods. A class should only be created if it makes sense to do so.

```Ruby
# wrong
class UserClass
    def self.some_method
        # content starts here
    end

    def self.some_other_method
        #content starts here
    end
end

# right
module SomeModule
    module_function

    def some_method
        #content starts here
    end

    def some_other_method
        #content starts here
    end
end

```

* The **attr** functions must be used to define trivial accessors or mutators.

```Ruby
#wrong
class OneClass
    def initialize(value, date)
        @date = date
        @date = date
    end

    def value
        @value
    end

    def date
        @date
    end
end

#right
class OneClass
    attr_reader :value, :date

    def initialize(value, date)
        @value = value
        @date = date
    end
end
```

* **attr_reader** and **attr_accessor** must be used instead of **attr**.

```Ruby
# wrong
attr :value, true
attr :one, :two, :three

# right
attr_accessor :value
attr_reader :one, :two, :three
```

* Class variables **@@** must not be used.

* Visibility levels to methods, like **public**, **protected**, **private**, must be used properly, depending on the method and its functionality and objective.

* The visibility method must be indented on the same level as the method they apply to. One blank line must be used above and below the visibility level.

```Ruby
class Payment
      def public_method
            #content starts here
      end

      private

      def another_private_method
            #content starts here
      end
end
```

* `self.method` must be used to define class methods.

```Ruby
Class User
    self.user_self_method
        #content starts here
    end
end
```

# 7. Exceptions

* Exceptions are signaled with the fail method. The raise method must be used only when purposely raising the exception.

* **RuntimeError** must not be explicitly specified in **fail**/**raise**.

* **fail**/**raise** must not be used with an exception instance, instead being used with an exception and a message as arguments.

```Ruby
# wrong
fail PaymentException.new('message')
# Note that there is no way to do `fail SomeException.new('message'), backtrace`.

# right
fail PaymentException, 'message'
# Consistent with `fail SomeException, 'message', ba´cktrace`.
```

# 8. Collections

* Array and hash creation notation must be used in its literal form.

```Ruby
# wrong
array = %w(here have an array)

# right
array = [ 'here',  'have',  'an', 'array' ]
```


* Comma after the last item of an array or hash must not be used.

```Ruby
# wrong
array = [ 'here',  'have',  'an', 'array
', ]

# right
array = [ 'here',  'have',  'an', 'array' ]
```

* `first` and `last` must be used accessing the first or last item of an array or hash, instead of [0] or `[-1]`.

```Ruby
#wrong
First_element = array[0]

#right
First_element = array.first
```

* Symbols must be used instead of strings as hash keys, unless for some reason unavoidable.

```Ruby
# wrong
hash = { 'key1' => 1, 'key2' => 2, 'key3' => 3 }

# right
hash = { key1: 1, key2: 2, key3: 3 }
```

* Hash keys must follow the Ruby 1.9 hash literal syntax , being composed of the symbol name, followed by a colon and the key value.

```Ruby
#wrong
hash = { :key1 => 1, :key2 => 2, :key3 => 3 }

# right
hash = { key1: 1, key2: 2, key3: 3 }
```

* If there is a key that is not a symbol in a hash, the hash rocket syntax must be used for all keys instead of the Ruby 1.9 hash literal syntax.

```Ruby
#wrong
{ key_a: 1, 'key_b': 2 }

#right
{ :key_a => 1, 'key_b' => 2 }
```

# 9. References

        https://github.com/bbatsov/rails-style-guide
