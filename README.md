# experiment-image-csp

Studying how Content Security Policy works with SVG images.

## How to run

- Create a new GitHub Codespaces
- Run `npm start`
- Browse to http://localhost:3000/

## Conclusion

- `script-src 'none'` can effectively disable scripts inside SVGs, including inline scripts like `<a href="javascript:...">`
- `style-src 'none'` can effectively disable embedded CSS stylesheet and `style` attribute inside SVGs
- CSS stylesheets in SVG will not leak if they are embedded via `<img>` or `<object>`
   - It will leak if the SVG is inlined in the HTML file
