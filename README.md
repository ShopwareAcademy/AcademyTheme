# AcademyTheme

This theme plugin contains the reference implementation for the **Theme Settings** learning unit in the Shopware Academy **Frontend Development Essentials** learning path.

## Reference State

The `LU-02-theme-configurations` tag represents the final file state of the learning unit. It demonstrates how to:

- Define a configurable color setting in `theme.json`.
- Organize the setting with a tab, block, section, and field.
- Make the saved setting available to SCSS as a variable.
- Use the configured color for the Storefront main navigation.

This reference state builds on the theme structure from the **Creating a Theme** learning unit. Compare its `theme.json` and `base.scss` with the files in the theme that you created yourself.

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

## Configure and Verify the Theme

Open the Theme Manager in the Shopware Administration:

- Go to **Sales Channels > Storefront > Theme** and select **Edit theme** for `AcademyTheme`.
- Alternatively, go directly to **Content > Themes > AcademyTheme**.

Open the **Colours** tab, select a **Background Colour** under **Main Navigation**, and save the theme configuration.

Compile the theme after changing its SCSS:

```bash
shopware-cli project console theme:compile
```

Alternatively, run:

```bash
bin/console theme:compile
```

Reload the Storefront. The main navigation should use the selected background color.

## License

MIT License.

You may use this plugin in commercial and professional projects.
It is provided as an educational example and comes without a warranty and without support.

## Contributing

This plugin is part of the **Shopware Academy** curriculum.
