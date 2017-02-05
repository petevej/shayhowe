### Why am I doing this?

HTML and CSS is sometimes viewed as a stepping stone to JavaScript and the greatness of the web. Most people just skip straight to using Bootstrap framework and while that is ok in most instances, I really do want to understand how to customize the aesthetics of webpages before using ready-made tools.

### Useful code snippet library

#### Boilerplate HTML structure
```HTML
<!DOCTYPE html>
<html lang="en">
  <head>

    <meta charset="utf-8">
    <title>Page Title</title>
    <link rel="stylesheet" href="assets/stylesheets/main.css">

  </head>

  <body>

    <header>

      <nav>
        <ul>
          <li><a href="index.html">Home</a></li><!--
          --><li><a href="page1.html">Page 1</a></li><!--
          --><li><a href="page2.html">Page 2</a></li><!--
          --><li><a href="page3.html">Page 3</a><li>
      </nav>

    </header>

    <section>
    </section>

    <footer>

      <nav>
        <ul>
          <li><a href="index.html">Home</a></li><!--
          --><li><a href="page1.html">Page 1</a></li><!--
          --><li><a href="page2.html">Page 2</a></li><!--
          --><li><a href="page3.html">Page 3</a><li>
      </nav>

    </footer>

  </body>

</html>
```

#### CSS Reset from http://meyerweb.com/eric/tools/css/reset/

```CSS
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}
```

#### iframe elements for inserting google maps:

```HTML
<iframe src="https://www.google.com/maps/embed?pb=!1m5!3m3!1m2!1s0x880e2cb1da049173%3A0xa5c91d255a775f0b!2sHotel+Sax+Chicago%2C+North+Dearborn+Street%2C+Chicago%2C+IL!5e0!3m2!1sen!2sus!4v1388702493978"></iframe>
```

#### Form elements

Group all form elements using fieldset element:

```HTML
<fieldset>

</fieldset>
```

Text input form type can be used to collect name of the user. Required for mandatory field:

```HTML
<label>
  Name
  <input type="text" name="name" placeholder="Full name" required>
</label>
```

Email input form type can be used to collect email:

```html
<label>
  Email
  <input type="email" name="email" placeholder="Email address" required>
</label>

Dropdown select-option element can be used to select Quantity:

```html
<label>
  Number of Passes
  <select name="quantity" required>

    <option value="1" selected>1</option>
    <option value="2">2</option>
    <option value="3">3</option>
    <option value="4">4</option>
    <option value="5">5</option>

  </select>
</label>
```

Textarea element can be used to collect comments:

```html
<label>
  Comments
  <textarea name="comments"></textarea>
</label>
```

Table structure elements:

table
  thead
    tr
      th
  tbody
    tr
      td
  tfoot
    tr
      td

```html
<table>

  <caption>Table Title</caption>

  <!-- Column header for 4-column table -->
  <thead>
    <tr>
      <th scope="col" colspan="2">Column Header 1</th>
      <th scope="col">Column Header 2</th>
      <th scope="col">Column Header 3</th>
    </tr>
  </thead>

  <tbody>

  <!-- Row 1 with 4 columns -->
    <tr>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <!-- Row 2 with 4 columns -->
    <tr>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>

  <!-- Table footer section for totals -->
  <tfoot>
    <tr>
      <td colspan="3">Subtotal</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="3">Tax</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="3">Total</td>
      <td></td>
    </tr>

  </tfoot>

</table>
```

#### Main body CSS

```CSS
body {
  background: #293f50;
  color: #888;
  font: 300 16px/22px "Lato", "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

#### Navigation CSS

```CSS
/*
  ========================================
  Navigation
  ========================================
*/

.nav {
  text-align: right;
}

.nav li {
  display: inline-block;
  margin: 0 10px;
  vertical-align: top;
}

.nav li:last-child {
  margin-right: 0;
}
```

#### Typography CSS

```CSS
.logo {
  border-top: 4px solid #648880;
  float: left;
  font-size: 48px;
  font-weight: 100;
  letter-spacing: .5px;
  line-height: 44px;
  padding: 40px 0 22px 0;
  text-transform: uppercase;
}

input,
select,
textarea {
  font: 300 16px/22px "Lato", "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

#### Custom Grid System

```CSS
/*
  ========================================
  Grid
  ========================================
*/

*,
*:before,
*:after {
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
}
.container,
.grid {
  margin: 0 auto;
  width: 960px;
}
.container {
  padding-left: 30px;
  padding-right: 30px;
}
.grid,
.col-1-3,
.col-2-3 {
  padding-left: 15px;
  padding-right: 15px;
}
.col-1-3,
.col-2-3  {
  display: inline-block;
  vertical-align: top;
}
.col-1-3 {
  width: 33.33%;
}
.col-2-3 {
  width: 66.66%;
}

```

#### Clearfix Codes

```CSS
/*
  ========================================
  Clearfix
  ========================================
*/

.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}
```

#### Custom link aesthetics

```CSS
/*
  ========================================
  Links
  ========================================
*/

a {
  color: #648880;
  text-decoration: none;
}
a:hover {
  color: #a9b2b9;
}
p a {
  border-bottom: 1px solid #dfe2e5;
}
.primary-header a,
.primary-footer a {
  color: #fff;
}
.primary-header a:hover,
.primary-footer a:hover {
  color: #648880;
}
```

#### Custom buttons

```CSS
/*
  ========================================
  Buttons
  ========================================
*/

.btn {
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-weight: 400;
  letter-spacing: .5px;
  margin: 0;
  text-transform: uppercase;
}
.btn-alt {
  border: 1px solid #fff;
  padding: 10px 30px;
}
.btn-alt:hover {
  background: #fff;
  color: #648880;
}

.btn-default {
  border: 0;
  background: #648880;
  padding: 11px 30px;
  font-size: 14px;
}

.btn-default:hover {
  background: #77a198;
}
```

#### Footer section CSS

```CSS
/*
  ========================================
  Primary footer
  ========================================
*/

.primary-footer {
  color: #648880;
  font-size: 14px;
  padding-bottom: 44px;
  padding-top: 44px;
}
.primary-footer small {
  float: left;
  font-weight: 400;
}

```

#### Round offset image CSS

```CSS
.speaker-info img {
  border-radius: 50%;
  height: 130px;
  margin: -66px 0 22px 0;
  vertical-align: top;
}
```

#### Elaborate table treatment CSS

```CSS
/*
  ========================================
  Schedule
  ========================================
*/

table {
  margin-bottom: 44px;
  width: 100%;
}

table:last-child {
  margin-bottom: 0;
}

th,
td {
  padding-bottom: 22px;
  vertical-align: top;
}
th {
  padding-right: 45px;
  text-align: right;
  width: 20%;
}
td {
  width: 40%;
}
thead {
  line-height: 44px;
}
thead th {
  color: #648880;
  font-size: 24px;
}
tbody th {
  color: #a9b2b9;
  font-size: 14px;
  font-weight: 400;
  padding-top: 22px;
  text-transform: uppercase;
}
tbody td {
  border-top: 1px solid #dfe2e5;
  padding-top: 21px;
}
tbody td:first-of-type {
  padding-right: 15px;
}
tbody td:last-of-type {
  padding-left: 15px;
}
tbody td:last-of-type {
  padding: left:15px;
}
tbody td:only-of-type {
  padding-left: 0;
  padding-right: 0;
}
table a {
  color: #888;
}
table h4 {
  margin-bottom: 0;
}
.schedule-offset {
  color: #a9b2b9;
}

```

#### Full CSS Codes

```CSS
/* http://meyerweb.com/eric/tools/css/reset/
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}
body {
  line-height: 1;
}
ol, ul {
  list-style: none;
}
blockquote, q {
  quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}

/*
  ========================================
  Custom styles
  ========================================
*/

body {
  background: #293f50;
  color: #888;
  font: 300 16px/22px "Lato", "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
}

/*
  ========================================
  Grid
  ========================================
*/

*,
*:before,
*:after {
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
}
.container,
.grid {
  margin: 0 auto;
  width: 960px;
}
.container {
  padding-left: 30px;
  padding-right: 30px;
}
.grid,
.col-1-3,
.col-2-3 {
  padding-left: 15px;
  padding-right: 15px;
}
.col-1-3,
.col-2-3  {
  display: inline-block;
  vertical-align: top;
}
.col-1-3 {
  width: 33.33%;
}
.col-2-3 {
  width: 66.66%;
}

/*
  ========================================
  Clearfix
  ========================================
*/

.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}

/*
  ========================================
  Rows
  ========================================
*/

.row,
.row-alt {
  min-width: 960px;
}
.row {
  background: #fff;
  padding: 66px 0 44px 0;
}
.row-alt {
  background: #cbe2c1;
  background: -webkit-linear-gradient(to right, #a1d3b0, #f6f1d3);
  background:    -moz-linear-gradient(to right, #a1d3b0, #f6f1d3);
  background:         linear-gradient(to right, #a1d3b0, #f6f1d3);
  padding: 44px 0 22px 0;
}

/*
  ========================================
  Typography
  ========================================
*/

h1, h2, h3, h4 {
  color: #648880;
}
h1, h3, h4, h5, p {
  margin-bottom: 22px;
}
h1 {
  font-size: 36px;
  line-height: 44px;
}
h2 {
  font-size: 24px;
  line-height: 44px;
}
h3 {
  font-size: 21px;
}
h4 {
  font-size: 18px;
}
h5 {
  color: #a9b2b9;
  font-size: 14px;
  font-weight: 400;
  text-transform: uppercase;
}
strong {
  font-weight: 400;
}
cite,
em {
  font-style: italic;
}

/*
  ========================================
  Leads
  ========================================
*/

.lead {
  text-align: center;
}
.lead p {
  font-size: 21px;
  line-height: 33px;
}

/*
  ========================================
  Links
  ========================================
*/

a {
  color: #648880;
  text-decoration: none;
}
a:hover {
  color: #a9b2b9;
}
p a {
  border-bottom: 1px solid #dfe2e5;
}
.primary-header a,
.primary-footer a {
  color: #fff;
}
.primary-header a:hover,
.primary-footer a:hover {
  color: #648880;
}

/*
  ========================================
  Buttons
  ========================================
*/

.btn {
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-weight: 400;
  letter-spacing: .5px;
  margin: 0;
  text-transform: uppercase;
}
.btn-alt {
  border: 1px solid #fff;
  padding: 10px 30px;
}
.btn-alt:hover {
  background: #fff;
  color: #648880;
}

.btn-default {
  border: 0;
  background: #648880;
  padding: 11px 30px;
  font-size: 14px;
}

.btn-default:hover {
  background: #77a198;
}

/*
  ========================================
  Primary header
  ========================================
*/

.logo {
  border-top: 4px solid #648880;
  float: left;
  font-size: 48px;
  font-weight: 100;
  letter-spacing: .5px;
  line-height: 44px;
  padding: 40px 0 22px 0;
  text-transform: uppercase;
}
.tagline {
  margin: 66px 0 22px 0;
  text-align: right;
}
.primary-nav {
  font-size: 14px;
  font-weight: 400;
  letter-spacing: .5px;
  text-transform: uppercase;
}

/*
  ========================================
  Primary footer
  ========================================
*/

.primary-footer {
  color: #648880;
  font-size: 14px;
  padding-bottom: 44px;
  padding-top: 44px;
}
.primary-footer small {
  float: left;
  font-weight: 400;
}

/*
  ========================================
  Navigation
  ========================================
*/

.nav {
  text-align: right;
}

.nav li {
  display: inline-block;
  margin: 0 10px;
  vertical-align: top;
}

.nav li:last-child {
  margin-right: 0;
}

/*
  ========================================
  Home
  ========================================
*/

.hero {
  color: #fff;
  line-height: 44px;
  padding: 22px 80px 66px 80px;
  text-align: center;
}
.hero h2 {
  font-size: 36px;
}
.hero p {
  font-size: 24px;
  font-weight: 100;
}
.teaser a:hover h3 {
  color: #a9b2b9;
}

.teaser img {
  border-radius: 5px;
  display: block;
  margin-bottom: 22px;
  width: 100%;  /* 100% of the parent column width*/
}
/*
  ========================================
  Speakers
  ========================================
*/

.speaker-info {
  border: 1px solid #dfe2e5;
  border-radius: 5px;
  margin-top: 88px;
  padding-bottom: 22px;
  text-align: center;
}

.speaker {
  margin-bottom: 44px;
}

.speaker-info img {
  border-radius: 50%;
  height: 130px;
  margin: -66px 0 22px 0;
  vertical-align: top;
}

/*
  ========================================
  Venue
  ========================================
*/

.venue-theatre {
  margin-bottom: 66px;
}

.venue-hotel {
  margin-bottom: 22px;
}

.vanue-map {
  height: 264px;
}

/*
  ========================================
  Register
  ========================================
*/

.why-attend {
  list-style: square;
  margin: 0 0 22px 30px;
}

form {
  margin-bottom: 22px;
}

input,
select,
textarea {
  font: 300 16px/22px "Lato", "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
}

.register-group label {
  color: #648880;
  cursor: pointer;
  font-weight: 400;
}

.register-group input,
.register-group select,
.regiser-group textarea {
  border: 1px solid #c6c9cc;
  border-radius: 5px;
  color: #888;
  display: block;
  margin: 5px 0 27px 0;
  padding: 5px 8px;
}

.register-group input,
.register-group textarea {
  width: 100%;
}

.register-group select {
  height: 35px;
  width: 60px;
}

.register-group textarea {
  height: 78px;
}

/*
  ========================================
  Schedule
  ========================================
*/

table {
  margin-bottom: 44px;
  width: 100%;
}

table:last-child {
  margin-bottom: 0;
}

th,
td {
  padding-bottom: 22px;
  vertical-align: top;
}
th {
  padding-right: 45px;
  text-align: right;
  width: 20%;
}
td {
  width: 40%;
}
thead {
  line-height: 44px;
}
thead th {
  color: #648880;
  font-size: 24px;
}
tbody th {
  color: #a9b2b9;
  font-size: 14px;
  font-weight: 400;
  padding-top: 22px;
  text-transform: uppercase;
}
tbody td {
  border-top: 1px solid #dfe2e5;
  padding-top: 21px;
}
tbody td:first-of-type {
  padding-right: 15px;
}
tbody td:last-of-type {
  padding-left: 15px;
}
tbody td:last-of-type {
  padding: left:15px;
}
tbody td:only-of-type {
  padding-left: 0;
  padding-right: 0;
}
table a {
  color: #888;
}
table h4 {
  margin-bottom: 0;
}
.schedule-offset {
  color: #a9b2b9;
}

```
