## `kensa create my_addon --template sinatra`

this repository is a sinatra template application for use with the 
Heroku <a href="http://github.com/heroku/kensa">kensa</a> gem

clone it via:

    > gem install kensa
    > kensa create my_addon --template sinatra
    > cd my_addon
    > bundle install
    > foreman start

In a new window: 

    > kensa sso 1

And you should be in a Heroku Single Sign On sesion for your brand new addon! 
