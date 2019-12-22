### MVC
  - views directory like helpers, templates == views for rails
  - 


  request comes in, goes to the router, inspects URL request was accessing,
  routes request to specific part of application. 

migrations: mix ecto.gen.migration add_topics
run migrations: $ mix ecto.migrate
rollback: $ mix ecto.rollback

class definitions:
- controller: defmodule Discuss.TopicController do

code sharing set up in lib/discuss_web.ex

conn - short for connection, focal point of Phoenix applications. Represents
incoming request and outgoing request

schema is set in models

changeset: 

params object represents the changes we want to make to the object, the struct
is a representation of what we have in the database
  Discuss.Topic.changeset(struct, params)
  - changeset not only function, but an object #=> Ecto.Changeset
  - params \\ %{} #=> if params are nil, use empty map ( just || ) 
  - 

forms:
  <%= form_for @changeset, topic_path(@conn, :create), fn f -> %>
  - 
