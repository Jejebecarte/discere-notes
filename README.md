<h1 align="center">Discere Notes</h1>

<p align="center">A comprehensive set of grammar notes for Discere, my Latin learning website.</p>

<div align="center">
    <a href="https://github.com/Jejebecarte/discere-notes/blob/master/LICENSE">
        <img alt="License" src="https://img.shields.io/github/license/Jejebecarte/discere-notes">
    </a>
    <a href="https://github.com/Jejebecarte/discere-notes/forks">
        <img alt="GitHub forks" src="https://img.shields.io/github/forks/Jejebecarte/discere-notes">
    </a>
    <a href="https://github.com/Jejebecarte/discere-notes/stargazers">
        <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Jejebecarte/discere-notes">
    </a>
</div>

## Table of Contents

- [About](#about)
- [Contributing](#contributing)
  - [File Structure](#file-structure)
  - [Writing Notes](#writing-notes)
    - [Frontmatter](#frontmatter)
    - [MDX Components](#mdx-components)
  - [Submitting Changes](#submitting-changes)
  - [Issues and Bug Reports](#issues-and-bug-reports)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## About

Discere is a Latin learning website initially created over the span of 8 weeks for a school software development project. It hosts a series of vocabulary and grammar testers, and notes on the language focused on intermediate level Latin learners.

Notes are created publically in this repository, allowing users of the website to submit improvements, fixes and new content, before being bundled and compiled with the website when it deploys.

If this project helped you, drop a ⭐️!

## Contributing

All contributions are appreciated - PRs are welcome! If you find any issues, or would like to change or add some content, feel free to.

You may either edit these notes on GitHub, or more preferrably follow these steps to edit the notes locally:

1. Download [Git](https://git-scm.com/) and [VSCode](https://code.visualstudio.com/), and the [Prettier VSCode extension](https://prettier.io/docs/en/editors.html#visual-studio-code).

2. Fork, and then clone this repository using `git clone`.

3. Make your changes, and then commit them:

```bash
$ git add .
$ git commit -am "Your commit message"
$ git push
```

4. Open a [pull request](https://github.com/Jejebecarte/discere-notes/) to submit your changes.

### File Structure

Notes are grouped into general categories, found within the [notes directory](/notes/). The file path of each note corresponds to its URL when deployed.

> **Note**
> Some categories for minor areas of notes, such as pronouns and adjectives, have been merged with related categories, in this case 'nouns'

Notes may also be further organised into groups using [frontmatter](#frontmatter).

### Writing Notes

Content written for notes must be concise, targetted at intermediate level students, and free of extraneous information. Use established layour and formatting conventions found within this repository.

When using information and/or content from other sources, ensure:

- The content is copyright free OR under an open-source license free of modification and distribution restrictions
- You update the repository [acknowledgements](#acknowledgements) accordingly

#### Frontmatter

In addition to note content, frontmatter is required metadata written in [YAML](https://yaml.org/) that must appear at the beginning of every note.

| Name                | Type     | Description                          |
| ------------------- | -------- | ------------------------------------ |
| title<br>(required) | string   | The note and page title              |
| description         | string   | Page description for SEO             |
| keywords            | string[] | Keywords for SEO                     |
| group               | string   | Note group within category           |
| order               | number   | Custom order for notes (LOW -> HIGH) |

#### MDX Components

In addition to the [basic syntax](https://www.markdownguide.org/basic-syntax/) provided by Markdown, there are a number of custom built components that you may include to create rich content. When using these comopnents, ensure there is a new line between the opening and closing tags.

<details>

<summary>Custom MDX Components</summary>

- Callout \<type> [title]

| Name     | Type                                  | Description                                    |
| -------- | ------------------------------------- | ---------------------------------------------- |
| children | ReactNode                             | Callout content                                |
| type     | "danger" \| "info" \| "tip" \| "warn" | Sets colour, icon and default title of callout |
| title    | string                                | Custom title                                   |

- Translation \<latin> \<translations> [withArrow]

| Name         | Type     | Description                                                                        |
| ------------ | -------- | ---------------------------------------------------------------------------------- |
| latin        | string   | The latin text to display                                                          |
| translations | string[] | A list of English translations                                                     |
| withArrow    | boolean  | Place arrow before each translation, indicating increase in fluency or correctness |

- CaseDisplayTable \<type>

| Name | Type                                                                 | Description            |
| ---- | -------------------------------------------------------------------- | ---------------------- |
| type | "all" \| "nom" \| "voc" \| "acc" \| "gen" \| "dat" \| "abl" \| "loc" | The case(s) to display |

- VerbDisplayTable \<type>

| Name | Type                                                        | Description               |
| ---- | ----------------------------------------------------------- | ------------------------- |
| type | "fut" \| "fut-perf" \| "pres" \| "impf" \| "perf" \| "plup" | The verb tense to display |

</details>

### Submitting Changes

Before committing your changes, please ensure:

- Your code has been properly formatted by [Prettier](https://prettier.io/).
- Your code is free of typos, factual errors, and broken component blocks or links.
- Your commit message is clear, concise and accurate.

Once you have met all of the above conditions, create a [pull request](https://github.com/Jejebecarte/discere-notes/pulls) with a detailed description of your changes. From here your changes will be reviewed, and any additional edits made before they are merged to the master branch.

### Issues and Bug Reports

To submit an issue or bug, please contact me privately or open an issue [here](https://github.com/Jejebecarte/discere-notes/issues).

## Acknowledgements

Parts of this repository use content from the following sources:

- [Dickinson College Commentaries](https://dcc.dickinson.edu/) under CC BY-SA License.

## License

This is an open-source project licensed under the [GPL v3.0 License](/LICENSE).
