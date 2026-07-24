# Contributing

## Getting started

Install Hugo and run a live local server for modification:

```bash
hugo serve
```

## Style guide

All pages should start with the page title as the top heading, as following: 

```md
# Page Title {anchor=false}
```

Subheadings should then be used for subsequent chapters, such as the following:

```md
## Subheading 1

### Subheading 2

#### Subheading 3
```

## Creating new pages:

Pages should be placed in a relevant section, e.g. user guides in `using-apollo`. Create a new markdown page with the following: 

```md
---
title: "Page title"
weight: 4 
---
```

The `weight` value represents this is where in the list the page will be stored, starting from `1` at the top. You should make sure the order is relevant and does not conflict with other pages.

## Creating new sections:

Creating new sections should be done sparingly, ideally new pages should be placed Sections can be created as folders under `content/docs`, with a `_index.md` file containing the following content:

```md
---
title: "Section title"
weight: 4
bookCollapseSection: true
---
```

The `weight` value represents this is where in the list the section will be stored, starting from `1` at the top. You should make sure the order is relevant and does not conflict with other sections.

## AI use

Please see the [Apollo Generative AI policy](https://docs.getapollo.dev/docs/contributing/gen-ai/). 