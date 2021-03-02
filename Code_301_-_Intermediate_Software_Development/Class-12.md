# EJS

## References

https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt

(video on EJS partials) by WalkThroughCode

https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433

EJS Partials by Hensle Joseph Aug 6, 2016

## EJS Partials

"Partials come in handy when you want to reuse the same HTML across multiple views. Think of partials as functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file andinclude it wherever you need it."


- perfect candidates for partials are headers and footers because they remain the same from page to page

- creating partials :
    - inside the "views/partials/ folder 
        - create a "navbar.ejs"
            - only contain the HTML for the nav bar on each page 

        - create the same thing for the footer
    - now that they are created we can use them in our other .ejs files

- `<%-include(PARTIAL_FILE) %>` put this where you want the included content to be.

- the (-) is important