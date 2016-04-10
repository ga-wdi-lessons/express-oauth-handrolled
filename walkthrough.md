# Added sessions

- What is a session variable? Why is it called a "session" variable?
- What are the two new things being `require`d in this app? How do you install them?
- What does a session "secret" do?
- How does `connect-mongo` relate to sessions?

![#](images/session-install.png)

# Removed candidate create form

![#](images/rm-candidate-form.png)

![#](images/rm-candidate-route.png)

# Added environment variables

- What is an environment variable? Why is it called an "environment" variable?
- Why is it necessary to `gitignore` environment variables?
- What does the `process` variable do?

![#](images/env-sample-json.png)

![#](images/env-gitignore.png)

![#](images/env-require.png)

# Added Twitter environment variables

- What's the difference between a "key" and a "secret"?

![#](images/twitter-env-sample.png)

![#](images/twitter-env-require.png)

# Redirects to Twitter sign-in page

- What two new modules need to be installed in this step?
- What's a "querystring"?
- What does `qstring.parse` do?
- What are the two arguments in a `request` callback?
- Where does `req.session` "physically" save data?

![#](images/twitter-sign-in.png)

# Completes Twitter authentication process

- What's the relation between `app.get("/login/twitter/callback")` and the `t_callback_url` we've specified?
- What is `req.query`? How is it different from `req.params`?

![#](images/twitter-auth-complete.png)

# Fetches user data from API

- Why is all this OAuth information being saved to a single `req.session.t_oauth` object?

![#](images/twitter-api-user-data.png)

# Saves candidate to database

- Why use `findOneAndUpdate`? Why not just `create`?
- How should you choose which user data to actually save to the database?

![#](images/db-add-twitter.png)
![#](images/db-save-candidate.png)

# Displays username and picture

- Why is `app.use` called *middle*ware?
- What's the difference between `res.locals` and `req.session`?
- What's the purpose of the `next` function?

![#](images/view-image-and-username.png)
![#](images/candidate-to-locals.png)

# Added nav bar and signout

![#](images/add-navbar.png)
![#](images/add-signout.png)

# Added Twitter API test route

![#](images/twitter-test-route.png)

# Moved Twitter stuff to separate file

- What's the advantage of moving the Twitter stuff to a separate file?
- What is the `module.exports` in this file?

![#](images/separate-file-twitter.png)

- There's one line not shown in the below image of `index.js`. What is it? (Hint: it's in the first few lines of the file.)

![#](images/separate-files.png)

# Can edit/delete only if current user

- Not shown are the changes to `views/candidates-show.hbs`. Nothing needs to be deleted from that file -- some things just need to be inserted (and then re-indented). Can you figure it out? Keep in mind the title of this step!

![#](images/write-if-current-user.png)

# Only require env.json in development environment

- You don't have your `env.json` on Heroku. How else can you set environment variables on Heroku?

![#](images/env-json-in-development.png)
