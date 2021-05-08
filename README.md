# Vertcoin Site
This site is built with Hugo and intended to be used for Vertcoin. It is not an official site as of now so will not be used on the vertcoin.org domain

## How to Contribute
Easy! If you would like to propose a change, first check the issue page if anyone else has submitted the change. If the change does not exist, create a detailed issue for it.

If you would like to make changes, you can fork the repository and clone it onto your machine. Ensure you have the **extended version of Hugo** installed.  
In order to view the changes in real time, and to include draft pages run the following command:
```
hugo server -D
```

If you are adding a new section, by default it will be created as a Draft. You can create a new section by running the following command:
```
hugo new section-name.md
```
Pay close attention to the **order** as this defines where it will appear on the page. If you are trying to insert a new section between two already existing sections, you will also have to adjust the order for all of the sections that come after the one that is included.

Stylesheets are stored under `assets/css` and can be used with Hugo pipes to automatically genereate css files as such:
```
    {{ $sass := resources.Get "css/style.scss" }}
    {{ $style := $sass | toCSS | minify | fingerprint }}
```

## Todo
- [x] Create the Hugo base layout
- [ ] Create the pages named in the navigation
- [ ] Fix header so colors are visible outside of the index page
- [ ] Use i18n rather than hard-coded (and currently dummy/placeholder) text
- [ ] Replace images (instead of using picsum as placeholders)
- [ ] Add fonts (instead of using Google Fonts etc)
- [ ] Separate index specific (S)CSS from sitewide CSS
- [ ] Breakdown complex-section shortcode further (section-top, section-bottom, section-columns, etc)