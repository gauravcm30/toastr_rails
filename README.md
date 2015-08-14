# ToastrRails

This is an opninionated [toaster](http://codeseven.github.io/toastr/demo.html) asset gem.
It sets some defaults, adds support for flash messages and assumes you have a navbar.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'toastr_rails'
```

And then execute:

    $ bundle

## Usage

Add to your application.js and application.css:
  
    //= require toastr_rails

You can put this in your layout/application.html file if you want to chach flash messages in a toast: 

    = render 'toastr_rails/flash'

use toastr to display a toast for info, success, warning or error

```ruby
   // Display an info toast with no title
   toastr.info('Are you the 6 fingered man?')
```

Other options -> 

```ruby
// Display a warning toast, with no title
toastr.warning('My name is Inigo Montoya. You Killed my father, prepare to die!')

// Display a success toast, with a title
toastr.success('Have fun storming the castle!', 'Miracle Max Says')

// Display an error toast, with a title
toastr.error('I do not think that word means what you tink it means.', 'Inconceivable!')
```

## Defaults:

    // javascript
    toastr.options = {
      "closeButton": true,
      "debug": false,
      "progressBar": true,
      "positionClass": "toast-top-right",
      "showDuration": "300",
      "hideDuration": "1000",
      "timeOut": "5000",
      "extendedTimeOut": "1000",
      "showEasing": "swing",
      "hideEasing": "linear",
      "showMethod": "fadeIn",
      "hideMethod": "fadeOut"
    };

    // css
    #toast-container{
      top: 70px;
    }

For all other options you can visit [http://codeseven.github.io/toastr/](http://codeseven.github.io/toastr/)

## Contributing

1. Fork it ( https://github.com/[my-github-username]/toastr_rails/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
