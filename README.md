# Ruby on Rails Extension Pack (by RailsNotes)

> SPONSOR: [RailsNotes UI — templates & components for Ruby on Rails apps (railsnotesui.xyz)](https://railsnotesui.xyz)
>
> ARTICLE: [A decent VS Code + Ruby on Rails setup (railsnotes.xyz)](https://railsnotes.xyz/blog/vscode-rails-setup)

Quickly setup VS Code for Ruby on Rails development with this extension pack.

This extension pack installs the following extensions:

- [Language Server]
  - [Shopify Ruby LSP](https://marketplace.visualstudio.com/items?itemName=Shopify.ruby-lsp)
  - [Solargraph](https://marketplace.visualstudio.com/items?itemName=castwide.solargraph)
- [LSP Integrations]
  - [Stimulus LSP](https://marketplace.visualstudio.com/items?itemName=marcoroth.stimulus-lsp)
- [Linting / Formatting]
  - [Rubocop](https://marketplace.visualstudio.com/items?itemName=rubocop.vscode-rubocop)
  - [Standard](https://marketplace.visualstudio.com/items?itemName=testdouble.vscode-standard-ruby)
  - [Rufo](https://marketplace.visualstudio.com/items?itemName=jnbt.vscode-rufo)
- [Debugger]
  - [VSCode rdbg Ruby Debugger](https://marketplace.visualstudio.com/items?itemName=KoichiSasada.vscode-rdbg)
- [ERB formatting]
  - [VS Code ERB Beautify](https://marketplace.visualstudio.com/items?itemName=aliariff.vscode-erb-beautify)
  - [Simple Ruby ERB](https://marketplace.visualstudio.com/items?itemName=vortizhe.simple-ruby-erb)

### Installation

1. Install the following gems globally so they're available for their respective extension —

   ```sh
   gem install solargraph rufo ruby-lsp-rails
   ```

   > Note: If you're using the `rubocop` or `standard` extensions, you need to add their respective gem to your `Gemfile` for their extension to pick them up.
   >
   > - `bundle add standard`
   > - `bundle add rubocop`

2. To use the `rdbg/debugger` extension, set the environment variable in your Rails app:

   ```sh
   RUBY_DEBUG_OPEN=true
   ```

   If you're using a `Procfile.dev`, you'd do this (so that you can connect to `debugger` instances from either process):

   ```sh
   web: RUBY_DEBUG_OPEN=true bin/rails server -p 3000
   sidekiq: RUBY_DEBUG_OPEN=true bundle exec sidekiq
   ...
   ```

   Then open the VS Code _"Run and Debug"_ menu, click _"create a launch.json file"_ and pick _"Ruby (rdbg)"_ to create a file with the correct configuration.

   I've written an in-depth guide here — [Using Rails debugger/rdbg with VS Code](https://railsnotes.xyz/blog/rails-debugger-rdbg-vscode).
