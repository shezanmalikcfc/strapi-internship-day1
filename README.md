DevOps Internship – Day 1 Task for my Devops Internship with Pearlthoughts

Strapi Setup, Content Type Creation, and GitHub Deployment

This repository contains my Day 1 work for the DevOps Internship program.
The task included cloning the official Strapi repository, setting up Strapi locally, creating a sample content type, and pushing the project to GitHub.

1. Cloned the Official Strapi Repository

As instructed, I first cloned the official Strapi source code:

git clone https://github.com/strapi/strapi


This repository contains the Strapi framework itself.
Cloning it was required as part of the task, but I did not run the framework from this folder.

2. Created a Local Strapi Project

To run Strapi locally, I created a new project using the Strapi CLI:

npx create-strapi@latest my-strapi-app


(Alternatively, I could use yarn create strapi my-strapi-app.)

During setup, I selected SQLite as the database for simplicity.
After installation, I started the development server:

npm run develop


Strapi became available at:

Admin Panel: http://localhost:1337/admin

API Base URL: http://localhost:1337/api

On the first run, I created an admin user account as prompted.

3. Explored the Project Structure

After setting up the project, I opened it in VS Code and reviewed the structure.
Key folders include:

src/
 ├─ admin/        - Admin panel customizations
 ├─ api/          - APIs and content types
 ├─ extensions/   - Plugin overrides
config/           - Environment and database configuration
public/           - Static files
package.json      - Dependencies and scripts


The content type I created is located in:

src/api/article

4. Created a Sample Content Type

Using the Strapi Admin Panel, I created a new collection type named "Article".
The fields I added were:

title (short text)

content (rich text)

publishedAt (date)

After saving, Strapi automatically generated the schema file at:

src/api/article/content-types/article/schema.json


I also created a sample entry under the Article content type to verify that it was working.

5. Initialized Git and Pushed to GitHub

Inside the Strapi project folder, I initialized a Git repository:

git init
git add .
git commit -m "Initial Strapi setup with sample Article content type"


Then I created a new GitHub repository and pushed the project:

git remote add origin <your-repo-url>
git branch -M main
git push -u origin main