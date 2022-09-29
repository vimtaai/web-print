# Web Print

**Web print** is a collection of CSS classes and default formatting to create print-ready documents using HTML and CSS.

## Setup

Import the stylesheet to your HTML document.

```html
<link rel="stylesheet" href="path/to/web-print/index.css">
```

## Usage

Add pages to your document and print through your browser's print dialog. You can specify the orientation and size of the page with CSS classes. Class names are designed to form natural language-like classes. For available sizes see the [`styles/sizes.css`](styles/sizes.css) file.

```html
<div class="portrait a4 page">
  <!-- Document content goes here -->
</div>
```

> [!IMPORTANT]
When printing through your browser's print dialog, make sure to set the page size to the same as you specified with the variables, set the margins to none, and to allow printing backgrounds.

If you want to print multiple pages per sheet, you can also wrap pages with a `.sheet` element. The orientation and size of the sheet can also be specified with CSS classes.

```html
<section class="portrait a4 sheet">
  <acticle class="portrait 3x5 page"></article>
  <acticle class="portrait 3x5 page"></article>
  <acticle class="portrait 3x5 page"></article>
  <acticle class="portrait 3x5 page"></article>
</section>
```

You can also create multi-column layouts for your pages by specifying the number of columns up to five.

```html
<article class="portrait two column a4 page"></article>
```

> [!Tip]
Both `.column` and `.columns` work for specifying column count, use whichever makes you class sound more natural.

You can create new page sizes by setting the `--print-page-large-side` and `--print-page-small-side` CSS variables. Modifiers, such as `.portrait`, `.landscape` and `.double` will work automatically.

```css
.my-page-size {
  --print-page-large-side: 8in;
  --print-page-small-side: 4in;
}
```

## Contributing

All ideas, recommendations, bug reports, pull requests are welcome. :smile:
