Questions, to figure out:

- Create staging branch. 
    
- Differentiate between live and dev env, set master to live, staging to dev
    Need to set the `NODE_ENV` var somewhere. 
    Check by adding this in template:
    `{{ if eq (getenv "NODE_ENV") "development" }}You're in development!{{ else }} You're live! {{ end }}`
    If run `npm start --development` it still says I'm live.

    See more details here: https://github.com/netlify-templates/victor-hugo

- What's the difference between all the various build commands
    Eg: `npm run preview`, `npm start --development` etc

- Add links to and from admin

- Make it so that there's only one reference for each page

- Delete all templates, files etc that we don't need
