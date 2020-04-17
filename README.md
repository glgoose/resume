# Resume

An online résumé. [Demo Site](https://demo-resume.netlify.app)  

![a preview of the generated résumé as a website and in print](src/assets/images/demo/resume.png)  

## Features

* Fully Customizable
* Semantic HTML
* Accessible (WCAG AA) 
* [h-resume](http://microformats.org/wiki/h-resume) Microformat
* Spellcheck Linter
* Self-Contained (no external resources)
* Search Engine Optimized (meta, JSON-LD, etc...)
* Critical CSS Inlined
* Print Styles

## Getting Started

To install the necessary packages, run this command in the root folder of the site:

```
npm install
```

__Commands__  

* Run `npm start` for a development server and live reloading
* Run `npm run build` to generate a production build

Deploy a fork of this template to Netlify:

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/maxboeck/resume) 

## Customize your Résumé

To edit the content and design of your résumé, follow these steps:

### 1. Personal Details

Open `src/data/author.json` and edit the information describing yourself. The following properties are supported (optional properties can be removed from the JSON file):

<table>
    <thead>
        <tr>
            <th>Key</th>
            <th>Description</th>
            <th>Required</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>name</code></td>
            <td>your full name</td>
            <td>required</td>
        </tr>
        <tr>
            <td><code>occupation</code></td>
            <td>your job description</td>
            <td>required</td>
        </tr>
        <tr>
            <td><code>location</code></td>
            <td>your town/state</td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>avatar</code></td>
            <td>the file name of your profile photo. Must be located in <code>src/assets/images/</code></td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>pronouns</code></td>
            <td>your preferred <a href="https://en.wikipedia.org/wiki/Preferred_gender_pronoun">gender pronouns</a></td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>email</code></td>
            <td>your email address</td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>telephone</code></td>
            <td>your phone number</td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>skills</code></td>
            <td>an array of strings describing your skillset</td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>languages</code></td>
            <td>an array of objects describing your spoken languages; each object should include a <code>name</code> (e.g. "English") and <code>level</code> (e.g. "fluent") property</td>
            <td>optional</td>
        </tr>
        <tr>
            <td><code>social</code></td>
            <td>an array of objects for each social profile you want to link; each object should include a <code>name</code> (e.g. "Github"), <code>user</code> (e.g. "@maxboeck") and <code>url</code> (e.g. "https://github.com/maxboeck") property</td>
            <td>optional</td>
        </tr>
    </tbody>
</table>

### 2. Introduction

Open `src/introduction.md` and edit the text content of the file with your personal short introduction summary. Limit it to 2-3 sentences and convey your motivation.

Leave the `layout` and `permalink` data at the top in place, and save the file.

### 3. Work Experience & Education

The entries for the sections "work experience" and "education" are stored as markdown files in `src/entries/work` and `src/entries/education`.

Delete the demo files in there and create your own. Include the following [frontmatter](https://www.11ty.dev/docs/data-frontmatter/) data:

<table></table>

### 4. Meta Data & Design

Open `src/data/meta.json` and replace the `url` with the URL of your hosted résumé. You can also customize the language and color scheme here.

Supported properties are:

<table></table>

## SpellCheck

If you run the project locally in development, the content of your `introduction` and `entries` will be automatically spell-checked using your system default spellcheck engine.

Possible misspelled words will be announced as warnings in the console output, like so:

```
Linter: check spelling for "incorect"
```

## Credits

Thanks to [Eric Bailey](https://ericwbailey.design/) for his post ["How to not make a résumé in React"](https://ericwbailey.design/writing/how-to-not-make-a-resume-in-react.html), which gave me the idea.

## Colophon

* "Butler" headline font by [Fabian de Smet](https://fabiandesmet.com/portfolio/butler-font/) (CC BY-SA 4.0 [License](https://github.com/maxboeck/resume/tree/master/src/assets/fonts/Butler_ButlerStencil_FontLicense_v1_0.pdf))
* Avatar image generated by GAN at [thispersondoesnotexist.com](https://www.thispersondoesnotexist.com/).
