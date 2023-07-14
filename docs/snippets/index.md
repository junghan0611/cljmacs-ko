# Snippets - Common code templates

Snippets are names that expand to code or documentation, to minimise typing commonly used code pattern and can serve as a reminder of common Clojure forms.

![Spacemacs LSP snippets - deps snippets in completion menu](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemcs-snippets-completion-menu-deps-snippets.png)

The content of a snippet can be anything, from a simple piece of text or a more involved code structure with placeholders for tab stops. Practicalli also uses snippets for rich code blocks, documentation and helping organise code in a namespace.

Snippets can include code which is evaluated, allowing the snippet to tap into all the features of Emacs (Yasnippets) or Clojure (Clojure LSP).


## Clojure LSP snippets

Clojure LSP snippets are editor agnostic although the editor needs to provide a Clojure LSP client. Snippets support tab stops, placeholders with default values and can pull in a following form (`$current-form`).

[Built-in snippets](https://clojure-lsp.io/features/#snippets){target=_blank} appear in the completion menu when typing.

Custom snippets are defined in the Clojure LSP configuration using the `:additional-snipets` key.

[practicalli/clojure-lsp-config snippets](https://github.com/practicalli/clojure-lsp-config#custom-snippets){target=_blank .md-button}


## Emacs Yasnippets

[YASnippets](https://github.com/joaotavora/yasnippet/blob/master/doc/index.org){target=_blank} uses plain text templates and so are very easy to learn and write.  Snippets are specific to an Emacs major mode.  They include tab stops, placoders with default values and markers to ensure correct indentation.

++meta++ ++slash++ expands the text under the point by any of the methods registered with hippie-expand. Yasnippets is one of the methods registered.

++tab++ will jump through the expanded snippet if it contains markers.

For example, `defn` is a snippet that expands into the full function definition form, tab stops jump the cursor through the snippet to add specific values to quickly complete the specifics of that function definition.

Yasnippets can also execute Elisp code, opening up a large number of Emacs functions to use within a snippet.

Spacemacs automatically includes [snippets for many programming languages and text formats](https://github.com/AndreaCrotti/yasnippet-snippets){target=_blank}, including [snippets for Clojure](https://github.com/AndreaCrotti/yasnippet-snippets/tree/master/snippets/clojure-mode){target=_blank}.
