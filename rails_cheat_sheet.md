To create a new app:
In terminal:
rails new <app_name>

cd <app_name>

To create a controller:
rails generate controller <controller_name> #plural

To create a model:
rails generate model Name_model name:string price:integer
https://guides.rubyonrails.org/getting_started.html#mvc-and-you-generating-a-model

to use seeds.db:
product = Product.create(name: "apple", price: 2, description: "real fuji apple")

to create server and database: 

rails db:drop db:create db:migrate db:seed

routing: (in vscode)
get "/path_name" => "controller_name#method_within_controller"

controller: (in vscode)
example:
def all_products
    products = Product.all
    render json: products.as_json
  end


using http gem:
create rb file
require "http"
response = HTTP.get("link")
without_extra_header = response.parse(:json)

check console:
rails console
Products.all
https://guides.rubyonrails.org/active_record_basics.html#create
https://guides.rubyonrails.org/active_record_basics.html#read
https://guides.rubyonrails.org/active_record_basics.html#update
https://guides.rubyonrails.org/active_record_basics.html#delete