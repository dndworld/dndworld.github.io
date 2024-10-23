---
label: Developer FYI
order: 20
---

[!ref Developer Documentation](/docs/)

Check [!badge icon="mark-github" variant="dark" text="Developing From Your Machine"](/docs/local-dev/) for FYI specific to the preview server.

=== **Page Links**

Page links are derived by transforming the base file path to lowercase and replacing spaces with dashes, e.g. `Example Folder/Example File.md` -> `example-folder/example-file.md`. When you preview the site on your local computer, the link will still work if you only replace spaces with dashes, but not so on the GitHube Pages site. Be sure to use the latter format when linking internal files and images.

=== **Creating New Files**

### Metadata Boilerplate

```yml
---
label: ""
icon: ""
order: 0
---
```
- `label`: title that appears on left sidebar
- `icon`: appears on left sidebar ([see below](#icons-and-emojis))
- `order`: order within folder on left sidebar, where higher `order` means higher `position`. Default value: 0. Files of the same `order` are organized A-Z.

See the [Page Configuration documentation](https://retype.com/configuration/page/) for more options. Metadata syntax is based on YAML.

As a best practice, set `order` to a value with 1-2 zeroes at the end so it is easier to insert another page in between two existing pages.

==- **Retype Components**

A `<style>` tag should be placed outside of a Tab component, or its CSS properties will not be applied when the Tab is opened.

==- **Icons and Emojis**

Emojis are mainly used as icons alongside page titles and some headings.

### Best Practices

Emojis should not be placed in the title itself, but be added to the `icon` metadata field and prepended to the title via CSS using the `<style>` tag. `icon` will appear on the sidebar, the CSS on the page title, while the tab remains title-only. How this is implemented depends on the type of emoji, described below.

`<style>` should preferably be placed right after the YAML metadata for visibility.

### Standard Emojis

Standard emojis are provided by [Mojee](https://mojee.io/emojis/). The list is largely similar but not the same as Discord's.

Retype uses the same `:name:` syntax as Discord to insert emojis by name into page content.

To insert an emoji as an `icon`, you must quote-wrap it (either type) since `:` is a special character in YAML.

```yaml
---
icon: ":thumbsup:"
---
```

To insert an emoji before the page title, paste the template below into the page and replace the emoji character. Note that it *must* be the character; the `:name:` will not work.

```html
<style>
h1:before { 
  content: "👍 ";
}
</style>
```

### Octicons

Retype also provides support for [Octicons](https://retype.com/components/octicons/). [Check here](https://primer.github.io/octicons/) for a list of Octicons and their names.

These icons are SVGs, which is actually a special type of HTML code. This allows them to be configured to change color with a theme, as Retype Octicons do when toggling dark mode.

Unfortunately, this means that Octicons cannot be inserted via CSS/`<style>`.

To insert an Octicon into page content, use `:icon-name:`, only replacing `name`.

To insert an Octicon as an `icon`, insert just the name (quote marks optional).

```yaml
---
icon: thumbsup
---
```

### Custom Emojis

For custom emojis, the image file must first be added to the source code, and the image file path is used to refer to it.

To insert a custom emoji into page content, use the template below and modify the `src` attribute as needed. Look for `.emoji` in `/_includes/head.html` for the styles used.

```md
<img class="emoji" src="/images/emoji-name.webp">
```

To insert a custom emoji as an `icon`, specify the file path:

```yaml
---
icon: "/images/emoji-name.webp"
---
```

To insert a custom emoji before the page title, use the template below and modify the `url()` argument as needed.

```html !#3
<style>
h1:before { 
  background: url('/images/emoji-name.webp') no-repeat 0 0;
  display: inline-block;
  content: "";
  width: 48px;
  height: 48px;
  margin-bottom: -8px;
  margin-right: 5px;
  background-size: 100%;
}
</style>
```

Additional Notes:
- `background` *must* precede `background-size`
- to place after the title, replace `:before` and `margin-right` with `:after` and `margin-left` respectively

==- **Styling**

Outside of images, CSS is used to control how the page content looks. You only really need to learn foundational concepts like selectors and the box model, then be ready to look up and read up on CSS properties. And a lot of testing of course. You should also [!badge icon="mark-github" variant="dark" text="set up a local fork on your machine"](/docs/local-dev) to preview changes.

`/_includes/head.html` contains some basic documentation.
- Retype's own styling will override or be re-applied when the reader jumps to a different page, so values for global styles must be appended with `!important` to not be ignored.

===

[!ref Developer Documentation](/docs/)