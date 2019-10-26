# Ruby & Ruby on rails

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Ruby & Ruby on rails](#Ruby--Ruby-on-rails)
	- [Rails Architecture guidelines](#Rails-Architecture-guidelines)
		- [Service objects](#Service-objects)
		- [Form objects](#Form-objects)
		- [Value objects](#Value-objects)
		- [Query objects](#Query-objects)
		- [Decorators / Delegators](#Decorators--Delegators)
	- [Tips and tricks](#Tips-and-tricks)
		- [Generate data in bulk](#Generate-data-in-bulk)
		- [Context on validations](#Context-on-validations)
	- [Resources](#Resources)
		- [Generic](#Generic)
		- [API](#API)
	- [Gems bookmarked](#Gems-bookmarked)
		- [Linting / Debug / DevOps](#Linting--Debug--DevOps)
		- [Utilities](#Utilities)
		- [API](#API-1)
		- [Code structure](#Code-structure)
		- [Form objects](#Form-objects-1)
	- [Divers](#Divers)
		- [Rails starters and generators](#Rails-starters-and-generators)
		- [Bundler](#Bundler)

<!-- /TOC -->

## Rails Architecture guidelines

Rails app architecture principles, as advised by I-cant-remember-who.
*To go deeper, see also "Architecture resources" in the Resources part, below.*

- **Models** : contains associations and constants. Callbacks are turned into **service objects**, validations are turned into **Form objects**
- **Controllers** : deals with HTTP routing, parameters parsing, authentication, content negotiation, calling the right service or editor object, exception catching, response formatting, and returning the right HTTP status code. The remaining -> **service objects**.
- **Helpers** : used for utility methods. Otherwise -> **Decorators**
- Always pass one instance variable per view.

### Service objects

- Called from controller.
- replaces model callbacks
- Services should call **Query objects**, and should not store state. Use instance methods, not class methods. There should be very few public methods in keeping with SRP.

### Form objects

Replaces ActiveRecord models naming and validations for the model

- [Active model form objects](https://robots.thoughtbot.com/activemodel-form-objects), Thoughbot

### Value objects

- to keep your code cleaner and to group related attributes
- use cases : money, date range
- Value objects should have multiple attributes.
- Attributes should be immutable throughout the object’s life cycle.
- Equality is determined by the object’s attributes.

### Query objects

- Query object methods should return an object, a hash or an array, not an ActiveRecord association.

### Decorators / Delegators

- great way to use polymorphism — providing different implementations for different contexts or types, over-riding or sub-classing helpers.
- replaces concerns too ?
- for specific use cases : formatting model attributes for any kind of presentation logic.
- Keep them light and breezy.

## Tips and tricks

### Generate data in bulk

```ruby
# times is an Enumerator
codes = 200.times.map { SecureRandom.hex(8) }
# equivalent to
codes = 200.collect.map { SecureRandom.hex(8) }
# equivalent to
codes = Array.new(200) { SecureRandom.hex(8) }
```

### Context on validations

```ruby
# app/models/user.rb
class User < ApplicationRecord
  attr_accessor :terms_of_service_accepted

  validates :terms_of_service_accepted, acceptance: true, on: :registration
end
```

```ruby
user.valid?(:registration)
user.save(context: :registration)
```

**Using Data Context Interaction**

```ruby
# app/models/user/registration_context.rb
module User::RegistrationContext
  def self.extended(model)
    class << model
      validates :terms_of_service_accepted, acceptance: true
    end
  end

  attr_accessor :terms_of_service_accepted
end
```

```ruby
user = User.find(id)
user.extend(User::RegistrationContext)
```

Source : [](https://karolgalanciak.com/blog/2018/06/24/rails-and-conditional-validations-in-models/)

## Resources

### Generic

- [Sandi Metz' Rules For Developers](https://robots.thoughtbot.com/sandi-metz-rules-for-developers)
- [Ruby on Rails, the iMenlo way](https://medium.com/imenlo/ruby-on-rails-the-imenlo-way-d29965618630#.ewxo0q9al)

**Books :**

- [99 Bottles](https://www.sandimetz.com/99bottles/) - Sandi Metz
- [11 Books Every Ruby on Rails Developer Should Read](https://www.netguru.co/codestories/11-books-every-ror-developer-should-read)
	- [Clean Code: A Handbook of Agile Software Craftsmanship ](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship-ebook/dp/B001GSTOAM) - Robert C. Martin
	- [The Pragmatic Programmer: From Journeyman to Master](https://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/020161622X) - Andrew Hunt, David Thomas
	- [Practical Object-Oriented Design](http://www.poodr.com/) - Sandi Metz
	- [The Rails 5 Way](https://www.amazon.com/Rails-Way-Addison-Wesley-Professional-Ruby/dp/0134657675) - Oble Fernandez

### Architecture & POROs :

- [Building maintainable Rails Apps](http://andypike.com/blog/conferences/rubyc-2016/) : form objects, command objects, query objects, presenter objects
- [Decoupling Rails Components](https://www.toptal.com/ruby-on-rails/decoupling-rails-components)
- [7 Patterns to Refactor Fat ActiveRecord Models](http://blog.codeclimate.com/blog/2012/10/17/7-ways-to-decompose-fat-activerecord-models/)
- [Enhanced Ruby on Rails Architecture](https://github.com/CodeRocketCo/enhanced-rails-architecture) : concerns, helpers, form object, decorators, policies, publisher-listener ,services
- [The Ultimate Intermediate Ruby on Rails Tutorial: Let’s Create an Entire App!](https://www.freecodecamp.org/news/lets-create-an-intermediate-level-ruby-on-rails-application-d7c6e997c63f/) : Authentication (with Devise), Ability to publish posts, and search and categorize them,  Instant messaging (popup windows and a separate messenger), with the ability to create private and group conversations, Ability to add users to contacts, Real time notifications

### API

- [JSON Serialization in Rails: A Complete Guide](https://buttercms.com/blog/json-serialization-in-rails-a-complete-guide)

## Gems bookmarked

### Linting / Debug / DevOps

- [rubocop](https://github.com/bbatsov/rubocop) : A Ruby static code analyzer, based on the community Ruby style guide
- [pronto](https://github.com/mmozuras/pronto) : Quick automated code review of your changes
- [reek](https://github.com/troessner/reek) : Code smell detector for Ruby
- [overcommit](https://github.com/brigade/overcommit) : A fully configurable and extendable Git hook manager
- [whenever](https://github.com/javan/whenever) : Cron jobs in Ruby
- [ahoy](https://github.com/ankane/ahoy) : Simple, powerful visit tracking for Rails
- [turnout](https://github.com/biola/turnout) : Turnout makes it easy to put Rack apps into maintenance mode
- [brakeman](https://github.com/presidentbeef/brakeman) : A static analysis security vulnerability scanner for Ruby on Rails applications mode
- [rack-mini-profiler](https://github.com/MiniProfiler/rack-mini-profiler) : Profiler for your development and production Ruby rack apps.
- [bullet](https://github.com/flyerhzm/bullet) : help to kill N+1 queries and unused eager loading


### Utilities
- [kaminari](https://github.com/kaminari/kaminari) : A Scope & Engine based, clean, powerful, customizable and sophisticated paginator for Ruby webapps (à la place de will_paginate ?)
- [sitemap_generator)](https://github.com/kjvarga/sitemap_generator) : framework-agnostic XML Sitemap generator written in Ruby with automatic Rails integration. It supports Video, News, Image, Mobile, PageMap and Alternate Links sitemap extensions and includes Rake tasks for managing your sitemaps, as well as many other great features.
- [ice_cube](https://github.com/seejohnrun/ice_cube) : Ruby Date Recurrence Library - Allows easy creation of recurrence rules and fast querying

### API
- [Json API rb](http://jsonapi-rb.org/) : Efficient and convenient JSON API library for ruby (upgrade of active model serializer, kind of)
- [Json API serializers](https://github.com/fotinakis/jsonapi-serializers) : Pure Ruby readonly serializers for the JSON:API spec.

### Code structure

- [interactor](https://github.com/collectiveidea/interactor) : common interface for performing complex user interactions. (made by CollectiveIdea)
- [trailblazer](https://github.com/trailblazer/trailblazer) : A High-Level Architecture for Ruby.
- [draper](https://github.com/drapergem/draper) : Decorators/View-Models for Rails Applications
- [wisper](https://github.com/krisleech/wisper) : A micro library providing Ruby objects with Publish-Subscribe capabilities

### Form objects

- [dry-validation](http://dry-rb.org/gems/dry-validation/basics/working-with-schemas/) ([github](https://github.com/dry-rb/dry-validation)) : Data validation based on predicate logic
- [Reform](https://github.com/trailblazer/reform) : Form objects decoupled from models

## Divers

- Exposing your localhost to the Internet : https://www.sitepoint.com/adding-sms-capabilities-to-your-rails-app/#gist2970916

- [Gist spec_helper to help finding leaks in tests ](https://gist.github.com/benoittgt/a13ad810f9fd21963fb8be9751ff7956)

### Rails starters and generators

- [rails starter template](https://github.com/dennybritz/rails_startup_template ) : script that installs basic gems with a wizard, with a few options
- [Rails Composer](https://github.com/RailsApps/rails-composer) The Rails generator on steroids for starter apps

### Bundler

- [A Guide to Update Gems with bundle update](https://medium.com/cedarcode/reduce-fear-of-bundle-update-with-this-4-step-process-e021e8808c48)