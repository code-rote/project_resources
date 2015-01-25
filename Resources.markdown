# Project Resources

### TO LEARN
  * SELF JOINS (comments on comments)
  * get it to colorize code
  * setup being able to hightlight a single line...highlight js
  * Versioning Models (Scores)
  * SingleTableInheritence (STI) - like polymorphic instead using single table.
<hr>

# HERE IS A CHANGE...

# Software Development Life Cycle (SDLC) Resources
### Source Code Control
  > [GitHub Flow on Trello](https://trello.com/b/Mm1rEv91/git)

### Agile Resources
> User Stories and a Product Backlog
  * [User Stories: An Agile Introduction](http://www.agilemodeling.com/artifacts/userStory.htm): 
  * [A Sample Format for a Spreadsheet-Based Product Backlog](http://www.mountaingoatsoftware.com/blog/a-sample-format-for-a-spreadsheet-based-product-backlog)
> Agile Software Development Process Examples
  * [Agile software development, steps to work with Requirements, Estimation and Planning](http://www.codeproject.com/Articles/674450/Agile-software-development-steps-to-work-with-Requ)

### Testing
  As a group we did not feel very comfortable with testing from the outset. However, there were some group members that were comfortable with the idea of User Stories and the power that comes from orienting the project deliverables from the view-point of the end-user instead of the developer. Moreover, we felt that the TDD material discussed in class was a bit too granular and would not be able to provide the correct testing structure to have us describe our functionality without digging deep into the weeds. Therefore, we decided to try to use RSpec's 'Feature Spec' functionality and make method_names longer and more descriptive in (as suggested by Chris Zetter in [How we write readable feature tests with RSpec](https://about.futurelearn.com/blog/how-we-write-readable-feature-tests-with-rspec/)). To make it work we had to use the Capybara gem and FactoryGirl.

> Getting Started with RSpec
  * [RSpec Quickstart Guide](/tutorials/Rails_Tutorials_RSpec_Quickstart_Guide.pdf)
  rspec-rails (https://github.com/rspec/rspec-rails) – installs RSpec gems with support for Rails
* [factory_girl_rails](https://github.com/thoughtbot/factory_girl_rails) – creates test data 
* [capybara] (https://github.com/jnicklas/capybara) – tests web pages
* [database_cleaner] (https://github.com/bmabey/database_cleaner) – a clean slate for databases
* [launchy] (https://github.com/copiousfreetime/launchy) – view errors in your web browser 
* [selenium-webdriver] (http://docs.seleniumhq.org/projects/webdriver/) – for tests that require JavaScript

> [Capybara Docs](http://rubydoc.info/github/jnicklas/capybara/master)
> RSpec's Feature Spec
  * [How we write readable feature tests with RSpec](https://about.futurelearn.com/blog/how-we-write-readable-feature-tests-with-rspec/)
  * [Feature Spec](https://relishapp.com/rspec/rspec-rails/v/3-0/docs/feature-specs/feature-spec)
  * [Capybara](http://www.rubydoc.info/github/jnicklas/capybara/master)

> Additional BDD and RSpec Articles
  * [BDD with Rspec and Steak](http://timelessrepo.com/bdd-with-rspec-and-steak)
  * [Setting up the BDD stack on a new Rails 4 app](https://semaphoreapp.com/blog/2013/08/14/setting-up-bdd-stack-on-a-new-rails-4-application.html)
  




# Front-end
## Front-end Design Decision-Making Resources & Tools
>* [Responsive CSS Framework Comparison](http://responsive.vermilion.com/compare.php)
>* [MaterialPalette](http://www.materialpalette.com/)

[Google Material Design](http://www.google.com/design/spec/material-design/introduction.html)
>* [Color](http://www.google.com/design/spec/style/color.html)
>* [Typography](http://www.google.com/design/spec/style/typography.html)
>* [Components](http://www.google.com/design/spec/components/bottom-sheets.html)
>* [Resources - Roboto & Noto fonts](http://www.google.com/design/spec/resources/roboto-noto-fonts.html)

## Front-end Targeted Platforms
>* Macbook Pro Retina 13" - 
MacBook Pro (Retina, 13-inch, Late 2012 and later) displays have a 2560-by-1600 native resolution at 227 pixels per inch with support for millions of colors.

>* Macbook Pro 13" (non-retina)


### Front-end Framework
  Requirements for front-end framework
  
  >1. responsive capabilities built-in
  >2. compatible with modern browsers
  >3. 

  We did not want to use the same bootstrap framework as the rest of the class. So we looked for similar front-end frameworks that would help us to stand out. We settled on Foundation because of prior experience and the general appeal of it's default styles and capabilities compared to bootstrap. If possible, we may try to take the built-in styles of Foundation for Apps and make them conform more to the Material Design philosophy promoted by Google.

> [Foundation 5](http://foundation.zurb.com/)
  * [The Kitchen Sink - Everything](http://foundation.zurb.com/docs/components/kitchen_sink.html)
> [Foundation for Apps](http://foundation.zurb.com/apps/index.html)
  * [Templates](http://foundation.zurb.com/apps/resources.html)
> [Material Foundation](https://github.com/eucalyptuss/material-foundation)

### Syntax Highlighting
  Requirements for syntax highlighter functionality:
  
  >1. Highlight appropriate syntax based on (a) file extension, or (b) an in-line html attribute. 
  >2. Compatibility with other third-party javascript libraries and frameworks.
  >3. Ability to highlight a single line
  >4. Ability to see the line number
  >5. Built in themes that are easy to change (will provide feature for user to customize their gameboard)

  We found two JS libraries that provide syntax highlighting based on regex matching and customized css and will meet the most important requirements listed above. _Prism.js_ seems to be a bit more robust with its library of plug-ins, but _highlight.js_ has declared simplicity as its design philosophy which means it should be easier to implement and get our MVP up and running without much configuration. For example, it automatically does language detection which likely means the package is bigger, but does not need to be fine-tuned from the outset. While it does not include the line numbering as part if its library, that is not going to break the MVP. 

#####[highlightJS](https://highlightjs.org/)
  >* [Getting Started Doc](https://highlightjs.org/usage/)
  >* [Full Documentation](http://highlightjs.readthedocs.org/en/latest/)
   * **[Library API - Core functions](http://highlightjs.readthedocs.org/en/latest/api.html)**: Primary reference point for implementing the library into our project.
   * [CSS class reference](http://highlightjs.readthedocs.org/en/latest/css-classes-reference.html)
   * [Style Guide](http://highlightjs.readthedocs.org/en/latest/style-guide.html)
  * [Dev's take on Lack of linenumber support](http://highlightjs.readthedocs.org/en/latest/line-numbers.html): in short - purpose of this library is simplicity, not robustness.

#####[PrismJS](http://prismjs.com/): Customize the download [here](http://prismjs.com/download.html)
  
  >[__1. Plugin Library__](http://prismjs.com/#plugins)
  >* [line highlight](http://prismjs.com/plugins/line-highlight/): Highlights specific lines and/or line ranges.
  >* [line numbers](http://prismjs.com/plugins/line-numbers/): Line number at the beginning of code lines.
  >* [highlight keywords](http://prismjs.com/plugins/highlight-keywords/): fine-grained control over css of keywords. Plug-in appends a css class to each keyword, e.g. 'if' will get '.keyword-if'. Could be useful for emphasizing the different keywords in a given step.
  >* [file highlight](http://prismjs.com/plugins/file-highlight/): Fetch external files and highlight them with Prism. Used on the Prism website itself. Would allow us to store the exercises as individual files instead of inline.
  >* [Autolinker](http://prismjs.com/plugins/autolinker/): Converts URLs and emails in code to clickable links. Parses Markdown links in comments.

  >__2. Limitations__
  >* [Limitation of Prism](http://prismjs.com/index.html#limitations)

  >[__3. Tutorials__](http://prismjs.com/#tutorials)
  >* [How To Re-Run Prism.js On AJAX Content](http://schier.co/blog/2013/01/07/how-to-re-run-prismjs-on-ajax-content.html)
  >* [Syntax highlighting with prism.js](http://www.kevinlorenz.com/home/prism_js)
  >* [Prism JS Code Highlighter](http://davidpeach.co.uk/prism-js-code-highlighter/)
  >* [Highlight your code with Prism](http://www.semisedlak.com/article/highlight-your-code-syntax-with-prismjs/)




# Additional Resources
## Cloud-based IDE
> Initially the product idea included a real-time code submission element. This would naturally lead us towards implementing a cloud-based IDE. However, we pivoted after determining that our primary focus would be learning by rote (repetition, repetition, repetition) instead of free-form as many other services already offer free-form and hint-based learning products. After the pivot, we stopped pursuing additional cloud editors. However, it is helpful to retain the resource links below for future reference.

> [Cloud9](https://c9.io/): Cloud service that provides both (a) an online code editor, and (b) a 'full' Ubuntu workspace in the cloud.
  * [Documentation](https://docs.c9.io/)
  * [Built on top of Ace editor](https://github.com/ajaxorg/ace)

>[Orion by Eclipse](http://eclipse.org/orion/)
  * [Getting started with Orion](http://wiki.eclipse.org/Orion/Getting_Started_with_Orion)










