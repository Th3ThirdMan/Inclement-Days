## Site Overview

This project is a weather forecasting website implementing hardcoded static data for selected cities. It makes use of reuseable components to present detailed information on specific cities. The aim of the project was to build a multi-page weather forecasting website using Eleventy and Bulma. There is no server-side functionality, apart from a final deployment to Netlify.

## Planning Stage
### Target Audience

Users interested in finding out the weather forecast in selected countries.
Users who need to access a 7-day weather forecast.

### First-time Visitors

Users should immediately understand the purpose of the site.
The website should be easy to navigate.

## Technologies Used

- HTML
- CSS
- Eleventy (11ty)
- Bulma
- Netlify

## Design and Features

I felt a dark theme would suit this project, with the icons serving well as a good contrast to a shadowed backdrop. The site is designed as a multi-page application with reusable weather cards created using Nunjucks. There are city specific weather forecast pages for selected cities. Also added is a link to show a weekly summary for all the cities. I employed the use of Bulma for layout and structure, coupled with custom CSS media queries to allow for responsiveness on smaller devices. 

## Project Structure

- `index.njk` – Home page
- City pages (`dublin.njk`, `paris.njk`, `cork.njk`, `lisbon.njk`)
- `summary.njk` – Weekly summary page
- `_includes/` – Shared layout and components (nav, footer, cards)
- `css/` – Site styling
- `images/` – Static images

## Development

To run the project locally:

```bash
npx @11ty/eleventy --serve
```

## Deployment

Project is deployed here: https://inclement-days.netlify.app/


## Challenges & Solutions

One challenge encountered during development was an issue with content not rendering correctly when using the Eleventy layout system. This occurred when the {{ content | safe }} placeholder was omitted from the main layout file, which prevented page content from being injected into the layout. This was resolved by correctly reinstating the placeholder in the layout template.

Another challenge involved navigation and routing for city-specific pages. Initially, some city pages did not render correctly due to missing or incorrectly structured index.njk files. This was resolved by ensuring each city page followed Eleventy’s expected folder and file structure, allowing navigation links to route correctly.

A further challenge related to navigation styling. Due to project constraints, JavaScript could not be used, and Bulma’s default dropdown navigation relied on JavaScript and applied a white background that conflicted with the site’s dark theme - while it served as a workaround I felt the contrast in the dropdown too stark, so needed to omit this. This was resolved by implementing a simplified, custom navigation layout using CSS only, ensuring consistent styling and responsiveness across devices.

Finally, repeated weather information across multiple pages was managed by creating reusable Nunjucks components, allowing weather cards to be reused with different hardcoded data.

## References

Unicode https://unicode.org/emoji/charts/full-emoji-list.html

Bulma Documentation https://bulma.io/documentation/

Eleventy (11ty) Documentation https://www.11ty.dev/docs/

Nunjucks Templating Documentation https://mozilla.github.io/nunjucks/

Netlify Documentation https://docs.netlify.com/




