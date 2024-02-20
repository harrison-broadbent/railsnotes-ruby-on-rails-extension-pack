# Ruby on Rails Extension Pack (by RailsNotes)

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
- [ERB formatting]
  - [VS Code ERB Beautify](https://marketplace.visualstudio.com/items?itemName=aliariff.vscode-erb-beautify)
  - [Simple Ruby ERB](https://marketplace.visualstudio.com/items?itemName=vortizhe.simple-ruby-erb)

Install the following gems so they're available for their extension —

```sh
gem install solargraph rufo ruby-lsp-rails
```

> Note: If you're using the `rubocop` or `standard` extensions, you need to add their respective gem to your `Gemfile` for their extension to pick them up.
>
> - `bundle add standard`
> - `bundle add rubocop`
