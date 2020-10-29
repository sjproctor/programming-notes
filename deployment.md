# Netlify Process

- Logged in to the website with GitHub
- $ yarn global add netlify-cli
- $ netlify login
- Log in with GitHub username and password in the CLI
- $ netlify init (to create a new project on netlify)
- Setup steps, added the name of the app

Copied from terminal:
```
Admin URL: https://app.netlify.com/sites/cat-tinder-frontend  
URL:       https://cat-tinder-frontend.netlify.app
```

- Authorized Netlify to access GitHub
- $ yarn run build
- ./build
- $ netlify deploy
- $ netlify deploy --prod


Redeploy with changes:
- Push changes to GitHub
- $ yarn run build
- $ yarn global add serve
- $ netlify deploy
- $ netlify deploy --prod


Adding React Router:
- Add a file to the public folder `_redirects`
- Add this code to the file: `/* /index.html 200`


# Heroku Process
- Create an account on Heroku
- $ brew tap heroku/brew && brew install heroku
- $ heroku login -i
- Enter email and password
- $ heroku create
- $ git config --list | grep heroku
- In the `config` directory there is a file called `master.key` (the file name might have a different color than others since it is included in the .gitignore)
- Copy the info in the `master.key` file and add it to this command in terminal
- $ heroku config:set RAILS_MASTER_KEY=<your-master-key>
- $ git push heroku master (or main, depending on your default branch name)
- $ heroku run rails db:migrate
- Check the heroku-url/cats to ensure the website launched correctly, mine showed an empty array (remember there are no cats in the production database)

# Connecting the Frontend
- Update the fetch request urls to make a request to the Heroku url
- Push changes to GitHub/Netlify
