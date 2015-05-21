# Devise-flash-messages-with-bootstrap-styles

Devise has two types of flash messages; notice, and alert. Most of my projects use Bootstrap so I want these Devise generated flash messages to appear with the Bootstrap alert styles. It's tempting to cook up an elaborate system involving keys and values but as there are only 2 we are working with I've used a couple of simple if statements.

## 1. Create a new partial to display your messages
1. Create a new file `app/views/layouts/_messages.html.erb`
2. Copy and paste the contents of the `_messages.html.erb` into your new file

## 2. Render the partial on each of your pages
1. Open `app/views/layouts/application.html.erb`
2. Add this line where you want your message to appear: `<%= render('layouts/messages.html.erb') %>`

## 3. Use `notice:` and `alert:` for your custom flash messages
* `redirect_to root_path, notice: 'This thing was successfully done.'`
* `redirect_to root_path, alert: 'Something went wrong.'`
