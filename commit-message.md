# Commit message guidelines

DCO (Developer Certificate of Origin)
Signing the DCO ensures the project that we have the right to use your code.
The most popular way to do DCO is to sign off your username and email address in the git command line.

First, configure your local git install.

$ git config --global user.name "John Doe" 
$ git config --global user.email johndoe@example.com
Obviously, you should use your own name and the email address associated with your GitHub user account.

Now, every time you commit new code in git, just add a signoff statement via the -s flag.

$ git commit -s -m "This is my commit message"


A good commit message should describe what changed and why.

1. The first line should:
   * contain a short description of the change (preferably 50 characters or
     less, and no more than 72 characters)
   * be entirely in lowercase with the exception of proper nouns, acronyms, and
   the words that refer to code, like function/variable names
   * be prefixed with the name of the changed subsystem and start with an
   imperative verb. Check the output of `git log --oneline files/you/changed` to
   find out what subsystems your changes touch.

   Examples:
   * `net: add localAddress and localPort to Socket`
   * `src: fix typos in doc.go`

1. Keep the second line blank.
1. Wrap all other lines at 72 columns (except for long URLs).

1. If your patch fixes an open issue, you can add a reference to it at the end
   of the log. Use the `Fixes:` prefix and the full issue URL. For other
   references use `Refs:`.

   Examples:
   * `Fixes: https://github.com/indykite/jarvis/issues/42`
   * `Refs: https://eslint.org/docs/rules/space-in-parens.html`
   * `Refs: https://github.com/indykite/jarvis/pull/88`

1. If your commit introduces a breaking change (`semver-major`), it should contain an explanation about the reason of the breaking change, which situation would trigger the breaking change and what is the exact change.

Sample complete commit message:

```text
athena: explain the commit in one line

The body of the commit message should be one or more paragraphs, explaining
things in more detail. Please word-wrap to keep columns to 72 characters or
less.

Fixes: https://github.com/indykite/jarvis/issues/42
Refs: https://eslint.org/docs/rules/space-in-parens.html
```

If you are new to contributing to IndyKite, please try to do your best at
conforming to these guidelines, but do not worry if you get something wrong.
One of the existing contributors will help get things situated and the
contributor landing the Pull Request will ensure that everything follows
the project guidelines.