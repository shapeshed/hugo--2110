# Test case for issue #2110

When a `.` character is included in a category name it breaks pagination and rendering.

Steps to reproduce

* Clone this repository
* Install a theme with categories e.g. `git clone https://github.com/carsonip/hugo-theme-minos.git themes/hugo-theme-minos`
* Generate the site `hugo server --theme=hugo-theme-minos`
* Click on a 'JavaScript' category link
* Observe this works correctly
* Return to homepage and click a 'Node.js' category link.
* Observe the page is not rendered correctly
* Paste `http://localhost:1313/categories/node.js/page/2/` into the address bar.
* Observe this is rendered correctly
* Change the address to `http://localhost:1313/categories/node.js/page/1/` and load the page
* Observe that raw HTML is rendered.


