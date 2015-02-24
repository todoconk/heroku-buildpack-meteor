# Heroku buildpack for meteor

## Usage

```
% heroku create --buildpack https://github.com/todoconk/heroku-buildpack-meteor.git
```

## Example

Create a sample app with 'meteor'

```
% meteor create --example todos
todos: created.

To run your new app:
   cd todos
   meteor
```

Put it in git.

```
% cd todos
% git init
Initialized empty Git repository in /tmp/a/todos/.git/
% git add .
% git commit -m "Sample todos app!"
```

Create your heroku app

```
% heroku create --buildpack https://github.com/todoconk/heroku-buildpack-meteor.git
```

Configure your plugins & settings
```
% heroku addons:add mongolab:sandbox
% heroku config:add MONGO_URL=<insert_value_of_MONGOLAB_URI_here>
% heroku config:add ROOT_URL=<insert_url_created_above_here>
```

Deploy it

```
% git push heroku
```

Enjoy!
