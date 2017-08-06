# Bestow: Foundation for Emails

Use case: Create document templates for insurance policies that are responsive, easy to layout and can be converted easily to dynamically populated PDF from Flask pdf to html. Also, they are cross-client compatible responsive emails.

-------------------------------------------------
<!--
Making dynamic for Intercom

{{ content }}
{{ unsubscribe_link }}
{{ unsubscribe_url }}
{{ first_name | fallback:"Reader" }}

{{ company.name | fallback:"Bestow" }}
{{ company.remote_company_id | fallback:"ENTER FALLBACK HERE" }}
{{ company.custom_data.name_of_attribute | fallback:"ENTER FALLBACK HERE" }}
 -->
-------------------------------------------------


## Full Guide to Foundation Ink
`http://foundation.zurb.com/emails/docs/sass-guide.html`

### Installing
We'll use the Foundation CLI to set up a new project. If you already have the Foundation CLI installed from Foundation for Sites, you can skip this first command.

### Copy
`npm install --global foundation-cli`
If you run into any permission errors (EACCESS) on OS X or Linux, you can try prefixing the command with sudo.

### Copy
`sudo npm install --global foundation-cli`
Once the CLI is installed on your machine, it’s super easy to fire up a blank Foundation for Emails project. Move into the folder you store your projects in, and then run this command:

### Copy
`foundation new --framework emails`
The CLI will ask you for a project name, which is used as the name of the folder to install in. After that, the project template will be downloaded, and the various dependencies installed. The entire process takes over a minute.

===

### Running the Server
After your project has been installed, run cd project, where project is the name of the project just created. Then run:

### Copy
`npm start`
This will kick off the build process, which includes HTML parsing, Sass, image compression, and a server. When the initial build finishes, your browser will pop open a new tab pointing to your project. You'll be seeing a blank index.html file.

### File Structure
You'll do all of your work in the src folder of your project. The various HTML files, Sass files, and images inside of src are compiled to a new folder called dist/ (as in "distribution"), which contains the final HTML and CSS for your emails. These are the files you'll upload to Litmus, Campaign Monitor, etc. for testing, or load into your email campaign service.

Here's a breakdown of the files in the src folder:

* `assets/`: Sass and image files.
* `layouts/`: Boilerplate HTML that wraps all of your emails.
* `pages/`: HTML files for emails.
* `partials/`: Reusable chunks of HTML that can be injected into pages.
