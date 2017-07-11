# Glossary

- __Attribute matchers__: An object describing the attributes shape of a block. The keys can be named as most appropriate to describe the state of a block type. The value for each key is a function which describes the strategy by which the attribute value should be extracted from the content of a saved post's content. When processed, a new object is created, taking the form of the keys defined in the attribute matchers, where each value is the result of the attribute matcher function.
- __Attributes__: The object representation of the current state of a block in post content. When loading a saved post, this is determined by the attribute matchers for the block type. These values can change over time during an editing session when the user modifies a block, and are used when determining how to serialize the block.
- __Block__: The abstract term used to describe units of markup that, composed together, form the content or layout of a webpage. The idea combines concepts of what in WordPress today we achieve with shortcodes, custom HTML, and embed discovery into a single consistent API and user experience.
- __Block name__: A unique identifier for a block type, consisting of a plugin-specific namespace and a short label describing the block's intent. e.g. `core/image`
- __Block type__: In contrast with the blocks composing a particular post, a block type describes the blueprint by which any block of that type should behave. So while there may be many images within a post, each behaves consistent with a unified image block type definition. 
- __Dynamic block__: A type of block where the content of which may change and cannot be determined at the time of saving a post, instead calculated any time the post is shown on the front of a site. These blocks may save fallback content or no content at all in their JavaScript implementation, instead deferring to a PHP block implementation for runtime rendering.
- __Editable__: A common component enabling rich content editing including bold, italics, hyperlinks, etc. It is not too much unlike the single editor region of the legacy post editor, and is in fact powered by the same TinyMCE library.
- __Inspector__: A block settings region shown in place of the post settings when a block is selected. Fields may be shown here to allow the user to customize the selected block.
- __Post settings__: A sidebar region containing metadata fields for the post, including scheduling, visibility, terms, and featured image.
- __Serialization__: The process of converting a block's attributes object into HTML markup, typically occurring when saving the post. 
- __Static block__: A type of block where the content of which is known at the time of saving a post. A static block will be saved with HTML markup directly in post content.
- __TinyMCE__: [TinyMCE](https://www.tinymce.com/) is a web-based JavaScript WYSIWYG (What You See Is What You Get) editor.
- __Toolbar__: A set of button controls. In the context of a block, usually referring to the toolbar of block controls shown above the selected block.