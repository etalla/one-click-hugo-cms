Questions, to figure out:

- DATA:
    - each datapoint should be created as a JSON within data folder 
    Here's an example table:
    <table>
    {{ range .Site.Data.[foldername]] }}
    <tr>
        <td>{{ .Name }}</td>
        <td>{{ .Employer }}</td>
        <td>{{ .Position }}</td>
    </tr>
    {{ end }}
    </table>

- Can links not be auto-generated, in footer and nav? 
    Ie when delete / create a page, shouldn't have to hard code each URL in those templates
    See maybe https://gohugo.io/templates/menu-templates/
    Or more simply sthing like the below (taken from https://gohugo.io/templates/lists/)
        <ul>
            <!-- Renders the li.html content view for each content/posts/*.md -->
            {{ range .Pages }}
            {{ .Render "li"}}
            {{ end }}
        </ul>

- Create staging branch. 
    
- Differentiate between live and dev env, set master to live, staging to dev
    Need to set the `NODE_ENV` var somewhere. 
    Check by adding this in template:
    `{{ if eq (getenv "NODE_ENV") "development" }}You're in development!{{ else }} You're live! {{ end }}`
    If run `npm start --development` it still says I'm live.

    See more details here: https://github.com/netlify-templates/victor-hugo

- What's the difference between all the various build commands
    Eg: `npm run preview`, `npm start --development` etc

- Add links to and from admin. Add favicon to admin.

- Make it so that there's only one reference for each page

- Delete all templates, files etc that we don't need

- Params:
    - Page params: declared in a md file under a folder and accessible to html file in that same folder. See https://gohugo.io/variables/page/#page-level-params
    - Site params: some are built in, others can be declared in config.toml