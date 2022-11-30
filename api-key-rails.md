# API Key for React in Rails

- Add to gemfile: `gem 'dotenv-rails'`
- $ `bundle`
- File in the root directory of the whole Rails project: `.env`
- In .env named exactly like this: `REACT_APP_API_KEY=abcd1234_my_api_key_here`
- Add `.env` to `.gitignore`
- Note: DO NOT COMMIT TO GITHUB BEFORE IGNORE
- In App.js: `console.log(process.env.REACT_APP_API_KEY)`
