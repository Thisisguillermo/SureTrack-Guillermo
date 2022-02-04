# Ruby (https://www.ruby-lang.org/en/)

*A dynamic, open source programming language with a focus on simplicity and productivity. It has an elegant syntax that is natural to read and easy to write.*

```
# The Greeter class
class Greeter
  def initialize(name)
    @name = name.capitalize
  end

  def salute
    puts "Hello #{@name}!"
  end
end

# Create a new object
g = Greeter.new("world")

# Output "Hello World!"
g.salute
```

`sudo apt-get install ruby-full`

`sudo apt install bundler`

## Ruby GEM (https://rubygems.org/) like NPM

*RubyGems.org is the Ruby community’s gem hosting service. Instantly publish your gems and then install them. Use the API to find out more about available gems. Become a contributor and improve the site yourself.*

**When you do gem install, it will search the current directory first, so if your .gem file is there, it will pick it up. I found it on the gem reference, which you may find handy as well:**

*gem install will install the named gem. It will attempt a local installation (i.e. a .gem file in the current directory), and if that fails, it will attempt to download and install the most recent version of the gem you want.*

## Ruby Bundler (https://bundler.io/)

*Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.Bundler is an exit from dependency hell, and ensures that the gems you need are present in development, staging, and production. Starting work on a project is as simple as bundle install.*
