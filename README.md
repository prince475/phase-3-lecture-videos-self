# Video: Self

<iframe src="https://player.vimeo.com/video/593996245/?title=0&byline=0&portrait=0" width="640" height="360" allowfullscreen="allowfullscreen" allow="autoplay; fullscreen; picture-in-picture"></iframe>

## Self code along

- In ruby 'self' points to the object that 'owns' the currently executing code.
- Here we are calling 'self' on both instances of 'price' and 'name' to allow us to add a list of ingredients to the add_ingredients method.
- This is possible since self can be used within an instance method to refer to the class instance on which that method is being called.

### The code below shows how self can be executed on a class instance


<code>require 'pry'</code>
<code>
class Coffee
  attr_reader :name
  attr_accessor :price, :ingredients
</code>
<code>
  def initialize(name, price = 2.50)
    @name = name
    @price = price
    @ingredients = []
  end
</code>
<code>
  def add_ingredients(ingredient)
    self.price += 0.50
    self.ingredients << ingredient
  end
end
</code>
<code>
c1 = Coffee.new('rose', 3.00)
c2 = Coffee.new('Tod')
binding.pry
</code>


### End
