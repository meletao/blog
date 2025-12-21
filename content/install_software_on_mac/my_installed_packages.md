# My Installed Packages

These are some packages I personally use.

<table border="1">
  <thead>
    <tr>
      <th>Software</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>tree</strong></td>
      <td>A recursive directory listing program that produces a depth-indented list of files (like a tree diagram).</td>
    </tr>
    <tr>
      <td><strong>zig</strong></td>
      <td>A general-purpose programming language and toolchain for maintaining robust, optimal, and reusable software.</td>
    </tr>
    <tr>
      <td><strong>uv</strong></td>
      <td>A fast Python package installer and resolver, intended as a drop-in replacement for <code>pip</code> and <code>pip-tools</code>.</td>
    </tr>
    <tr>
      <td><strong>visual studio code</strong></td>
      <td>A code editor developed by Microsoft.</td>
    </tr>
    <tr>
      <td><strong>git</strong></td>
      <td>A version control command-line tool. Installing this should also install Xcode command-line utilities.</td>
    </tr>
  </tbody>
</table>

To install them, run:
```zsh
brew install tree
brew install zig
brew install uv

brew install --cask visual-studio-code
brew install git
```

:::{note}
*--cask* flag tells brew to download package as GUI application instead of command-line tool.
:::
