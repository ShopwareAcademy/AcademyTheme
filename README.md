# AcademyTheme

This theme plugin contains the reference implementation for the **Override SCSS Variables** learning unit in the Shopware Academy **Frontend Development Essentials** learning path.

## Reference State

The `LU-03-override-scss-variables` tag represents the final file state of the learning unit. It demonstrates how to:

- Load `overrides.scss` before `@Storefront` in the `theme.json` style order.
- Override existing Shopware and Bootstrap SCSS variables before the storefront styles are compiled.
- Set the standard, small, and large border-radius variables to `5px`.
- Keep custom selectors in `base.scss` instead of adding them to `overrides.scss`.

This reference state builds on the `LU-02-theme-configurations` tag. The configurable navigation color from the previous learning unit remains part of the theme. The new LU03 implementation is the completed radius override in `overrides.scss`.

The theme configuration uses `label` translations in `theme.json` to remain aligned with the learning unit's supported Shopware versions. Shopware 6.7.16.0 may show a warning during `theme:refresh` that these translations were converted into Administration snippets. The warning does not mean that the refresh failed.

## Install and Assign

Run the following commands from your Shopware project root.

**Shopware CLI:**

```bash
shopware-cli project console plugin:refresh
shopware-cli project console plugin:install AcademyTheme --activate --clearCache
shopware-cli project console theme:refresh
shopware-cli project console theme:change
```

**Direct Shopware Console:**

```bash
bin/console plugin:refresh
bin/console plugin:install AcademyTheme --activate --clearCache
bin/console theme:refresh
bin/console theme:change
```

Run only one command variant. In the interactive `theme:change` command, select `AcademyTheme` and then the Storefront sales channel that should use it.

## Compile and Verify the Override

The border-radius override does not add another setting to the Theme Manager. Its values are defined directly in `overrides.scss` and applied during theme compilation.

Compile the theme after installing or changing the reference state:

```bash
shopware-cli project console theme:compile
```

Alternatively, run:

```bash
bin/console theme:compile
```

Reload the storefront without the browser cache. Verify the rounded corners across standard, small, and large components in several views, including the product listing, cart, and offcanvas cart.

Compare `overrides.scss` with your own theme. It should contain:

```scss
$border-radius: 5px;
$border-radius-sm: 5px;
$border-radius-lg: 5px;
```

## License

MIT License.

You may use this plugin in commercial and professional projects.
It is provided as an educational example and comes without a warranty and without support.

## Contributing

This plugin is part of the **Shopware Academy** curriculum.
