# Resources


# TO LEARN
SELF JOINS (comments on comments)
get it to colorize code
setup being able to hightlight a single line...highlight js
Versioning Models (Scores)
SingleTableInheritence (STI) - like polymorphic instead using single table.

# Software Development Life Cycle (SDLC) Resources
### Source Code Control
  > [GitHub Flow on Trello](https://trello.com/b/Mm1rEv91/git)

### Agile Resources
  > [Agile Modeling: User Stories: An Agile Introduction](http://www.agilemodeling.com/artifacts/userStory.htm): 
  > [A Sample Format for a Spreadsheet-Based Product Backlog](http://www.mountaingoatsoftware.com/blog/a-sample-format-for-a-spreadsheet-based-product-backlog)

### Testing
  > [BDD with Rspec and Steak](http://timelessrepo.com/bdd-with-rspec-and-steak)
  > [Setting up the BDD stack on a new Rails 4 app](https://semaphoreapp.com/blog/2013/08/14/setting-up-bdd-stack-on-a-new-rails-4-application.html)
  > 

# Front-end
## Front-end Design Decision-Making Resources & Tools
> [Responsive CSS Framework Comparison](http://responsive.vermilion.com/compare.php)
> [MaterialPalette](http://www.materialpalette.com/)
> [Google Material Design](http://www.google.com/design/spec/material-design/introduction.html)
  >* [Color](http://www.google.com/design/spec/style/color.html)
  >* [Typography](http://www.google.com/design/spec/style/typography.html)
  >* [Components](http://www.google.com/design/spec/components/bottom-sheets.html)
  >* [Resources - Roboto & Noto fonts](http://www.google.com/design/spec/resources/roboto-noto-fonts.html)

### Front-end Framework
> Requirements for front-end framework
  1. responsive
  2. compatible with modern browsers
  3. 

> We 
> [Foundation 5](http://foundation.zurb.com/)
  * [The Kitchen Sink - Everything](http://foundation.zurb.com/docs/components/kitchen_sink.html)
> [Foundation for Apps](http://foundation.zurb.com/apps/index.html)
  * [Templates](http://foundation.zurb.com/apps/resources.html)
> [Material Foundation](https://github.com/eucalyptuss/material-foundation)

### Syntax Highlighting
> Requirements for syntax highlighter functionality:
  1. Highlight appropriate syntax based on (a) file extension, or (b) an in-line html attribute. 
  2. Compatibility with other third-party javascript libraries and frameworks.
  3. Ability to highlight a single line
  4. Ability to see the line number
  5. Built in themes that are easy to change (will provide feature for user to customize their gameboard)

  > We found two JS libraries that provide syntax highlighting based on regex matching and customized css and will meet the most important requirements listed above. _Prism.js_ seems to be a bit more robust with its library of plug-ins, but _highlight.js_ has declared simplicity as its design philosophy which means it should be easier to implement and get our MVP up and running without much configuration. For example, it automatically does language detection which likely means the package is bigger, but does not need to be fine-tuned from the outset. While it does not include the line numbering as part if its library, that is not going to break the MVP. 

> [highlightJS](https://highlightjs.org/): main site
  * [Getting Started Doc](https://highlightjs.org/usage/)
  * [Full Documentation](http://highlightjs.readthedocs.org/en/latest/)
   * **[Library API - Core functions](http://highlightjs.readthedocs.org/en/latest/api.html)**: Primary reference point for implementing the library into our project.
   * [CSS class reference](http://highlightjs.readthedocs.org/en/latest/css-classes-reference.html)
   * [Style Guide](http://highlightjs.readthedocs.org/en/latest/style-guide.html)
  * [Dev's take on Lack of linenumber support](http://highlightjs.readthedocs.org/en/latest/line-numbers.html): in short - purpose of this library is simplicity, not robustness.

> [PrismJS](http://prismjs.com/): Customize the download [here](http://prismjs.com/download.html). Prism also has plug-in library.
  * [line highlight](http://prismjs.com/plugins/line-highlight/): Highlights specific lines and/or line ranges.
  * [line numbers](http://prismjs.com/plugins/line-numbers/): Line number at the beginning of code lines.
  * [highlight keywords](http://prismjs.com/plugins/highlight-keywords/): fine-grained control over css of keywords. Plug-in appends a css class to each keyword, e.g. 'if' will get '.keyword-if'. Could be useful for emphasizing the different keywords in a given step.
  * [file highlight](http://prismjs.com/plugins/file-highlight/): Fetch external files and highlight them with Prism. Used on the Prism website itself. Would allow us to store the exercises as individual files instead of inline.
  * [Autolinker](http://prismjs.com/plugins/autolinker/): Converts URLs and emails in code to clickable links. Parses Markdown links in comments.
  * [Limitation of Prism](http://prismjs.com/index.html#limitations)




# Additional Resources
## Cloud-based IDE
> Initially the product idea included a real-time code submission element. This would naturally lead us towards implementing a cloud-based IDE. However, we pivoted after determining that our primary focus would be learning by rote (repetition, repetition, repetition) instead of free-form as many other services already offer free-form and hint-based learning products. After the pivot, we stopped pursuing additional cloud editors. However, it is helpful to retain the resource links below for future reference.

> [Cloud9](https://c9.io/): Cloud service that provides both (a) an online code editor, and (b) a 'full' Ubuntu workspace in the cloud.
  * [Documentation](https://docs.c9.io/)
  * [Built on top of Ace editor](https://github.com/ajaxorg/ace)

>[Orion by Eclipse](http://eclipse.org/orion/)
  * [Getting started with Orion](http://wiki.eclipse.org/Orion/Getting_Started_with_Orion)










