# 🐟 Sardine Design Tokens
<img src="Preview.png" width=100% height=100%>

Sardine is a codename for rewamp of what was previously known as Anchovi tokens, a design system repository which stores design decisions at Morsum in a platform-agnostic way so they can be shared across different disciplines, tools and technologies.
At its core, design token is an information associated with a name and value, similar to a variable. It can also come with pre-defined type, description and reference to another design token or a tool.

## 🎯 Goals
- [x] Transition to better, up to date tools.
- [x] Give design system a name for easier reference - 🐟 Sardine.
- [x] Improve the clarity of token structure and provide the full calculations of their values.
- [x] Adopt the visual language of 2023 Brand Manual.
- [x] Support dynamic scales for size, spacing and typography.
- [x] Support for multi-dimensional themes, allowing users to swap brands and modes using token collections.

## 🗂️ Structure
### Tokens
**[Tokens](https://github.com/Morsum/sardine/tree/main/tokens)** are structured:
- **[core](https://github.com/Morsum/sardine/tree/main/tokens/core)** - default token sets.
- - **[colors](https://github.com/Morsum/sardine/tree/main/tokens/core/colors)** - color sets for different brands in their primitive form.
- **[density](https://github.com/Morsum/sardine/tree/main/tokens/density)** - token sets for global, alternative density modes.
- **[resources](https://github.com/Morsum/sardine/tree/main/tokens/resources)** - output of external tools that is then referenced or aliased in other token sets.
- **[themes](https://github.com/Morsum/sardine/tree/main/tokens/themes)** - contains semantic themes, each referencing parts or all of the other sets.
- **[themes definition](https://github.com/Morsum/sardine/blob/main/tokens/%24themes.json)** - a json configuration file that sets rules for each theme.

### Icons
Icons are have their own folder, and use following structure: `Style / Category / Icon`


## 🎨 Auto-generated themes
We can speed up the process to generate new themes with **[Leonardo](https://github.com/adobe/leonardo)** by setting the same contrast ratios as Anchovi and updating the color keys. Output is then exported into `resources / leonardo-export-[mode]` and then aliased in `themes / leonardo-[mode]` giving us the semantic tokens for new brand. [^1].
[^1]: Current setup is done manually using Leonardo's web tool. In the future, we want to create and run configurations in this repository to speed up the process and maintain the contrast ratio scales.

## 🔩 Format
Sardine's using updated formatting from Tokens Studio. All of the regular [W3C](https://github.com/design-tokens/community-group) token types are supported [^2] and there are couple of extended ones, mostly for certain Figma features or to group multiple tokens together. Formatting is set automatically by Tokens Studio, but we're able to alter folder structure and reference names of each token. They can be transformed using [sd-transforms](https://github.com/tokens-studio/sd-transforms) for Style Dictionary.
[^2]: Tokens Studio is in process of adopting the latest version of W3C spec right now, which is why some of the formatting is not up to date - most notably the token properties not being prefixed with $.

## 📁 Design resources
Check the **[design presentation](https://www.figma.com/proto/mIjxHH8d3MOG6fNJ636c55/Design-Tokens-2.0-presentations?page-id=0%3A1&type=design&node-id=1-661&viewport=645%2C261%2C0.15&t=b1yWxMG1ZQHYDSvt-1&scaling=contain&starting-point-node-id=1%3A661&mode=design)** or look at [Jira tickets](https://morsum.atlassian.net/browse/DEST-306).
