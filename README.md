# Personal site

Single static page. No build step, no dependencies.

## Publish on GitHub Pages (free)

1. Create a **public** repository named exactly `sowmyak4qa.github.io`
2. Push the contents of this folder to its root (`index.html`, `styles.css`,
   `.nojekyll`, the resume PDF)
3. GitHub serves it at `https://sowmyak4qa.github.io` within a minute or two

Run in one PowerShell window, in this order (the `cd` matters: one folder up
would publish the whole job-search folder):

```
gh auth login -h github.com
cd C:/Users/sowmy/Documents/JobSearch/site
git init
git config user.email sowmyak4qa@gmail.com
git config user.name "Sowmya Kuruvella"
git add .
git commit -m "Personal site"
gh repo create sowmyak4qa.github.io --public --source=. --push
```

## Keep the resume current

The PDF here is a copy of `../resume/Sowmya_Kuruvella_Resume.pdf` (the two-page primary).
After regenerating the resume, copy it over again and push.

## Optional: custom domain

A domain like `sowmyakuruvella.com` costs about $12/year and looks more
established than a github.io address. Add a file named `CNAME` containing the
domain, then point the domain's DNS at GitHub Pages per their docs.
