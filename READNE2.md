How would you return all the recipes in your database?
-Recipe.all

Recipe.all.each do |recipe|
  recipe.title
end


How would you return all the comments in your database?
-Comment.all

Comment.all.each do |comment|
  comment.body
end

How would you return the most recent recipe posted in your database?
-Recipe.first

How would you return all the comments of the most recent recipe in your database?
-Recipe.last.comments

OR

recipe = Recipe.last
comment = Comment.where(recipe_id: recipe.id)

How would you return the most recent comment of all your comments?
-Comment.last

How would you return the recipe associated with the most recent comment in your database?
-Comment.last.recipe

OR

comment = Comment.last
recipe = Recipe.where(id: comment.recipe_id)

How would you return all comments that include the string brussels in them?
-Comment.where(["body LIKE ?", "%brussels%"])

OR




Mentor Group Notes:
recipe5.comments.create(body: "") #this allows you to create a comment to that particular recipe;

This can be used in ERB
<% recipe.5.comments.each do |comment| %>
  <%= comment %>
<% end %>

timestamps creates created_at and updated_at
