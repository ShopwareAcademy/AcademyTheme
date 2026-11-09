# AcademyTheme

This theme plugin contains the reference implementations for the **Shopware Theme Development** course in the Shopware Academy Frontend Development Essentials learning path.

## Reference States

Each learning unit has a dedicated Git tag:

- `LU-01-creating-a-theme`: Create, install, assign, and verify a custom Shopware theme.
- `LU-02-theme-settings`: Add a configurable main navigation background color and use its value in SCSS.
- `LU-03-override-scss-variables`: Override existing Shopware and Bootstrap SCSS variables to apply a consistent border radius.

The `main` branch represents the final state after the third learning unit. It demonstrates how to:

- Define the theme resources and SCSS load order in `theme.json`.
- Organize a custom theme setting for the main navigation background color.
- Use the generated theme configuration variable in `base.scss`.
- Load variable overrides before `@Storefront`.
- Apply a consistent `5px` border radius through existing SCSS variables.
- Keep variable overrides in `overrides.scss` and custom selectors in `base.scss`.

The final state has been verified with Shopware 6.7.16.0.

## Install

Run the following commands from your Shopware project root.

**Shopware CLI:**

```bash
shopware-cli project console plugin:refresh
shopware-cli project console plugin:install AcademyTheme --activate --clearCache
shopware-cli project console theme:change
```

**Direct Shopware Console:**

```bash
bin/console plugin:refresh
bin/console plugin:install AcademyTheme --activate --clearCache
bin/console theme:change
```

Run only one command variant. When `theme:change` prompts you for a theme and a sales channel, select `AcademyTheme` and the storefront sales channel that should use it.

If the theme was already installed when you changed `theme.json` or the SCSS files, synchronize the configuration and compile the theme again:

**Shopware CLI:**

```bash
shopware-cli project console theme:refresh
shopware-cli project console theme:compile
```

**Direct Shopware Console:**

```bash
bin/console theme:refresh
bin/console theme:compile
```

## Verify the Final State

Open **Content > Themes > AcademyTheme** in the Shopware administration:

1. Open **Colours > Theme Colours > Main Navigation**.
2. Select and save a value for **Background Colour**.
3. Compile the theme and reload the assigned storefront.
4. Confirm that the main navigation uses the selected color.
5. Check common storefront controls such as buttons and form fields. Their border radius should be `5px`.

## License

MIT License.

You may use this plugin in commercial and professional projects. It is provided as an educational example and comes without a warranty and without support.

## Contributing

This plugin is part of the **Shopware Academy** curriculum.
