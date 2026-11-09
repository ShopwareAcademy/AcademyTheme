# AcademyTheme

This theme plugin contains the reference implementation for the **Creating a Theme** learning unit in the Shopware Academy **Frontend Development Essentials** learning path.

## Reference State

The `LU-01-creating-a-theme` tag represents the final file state of the learning unit. It demonstrates how to:

- Use the plugin structure for a Shopware theme.
- Register the theme through a plugin class that implements `ThemeInterface`.
- Define the theme's views, styles, scripts, and assets in `theme.json`.
- Provide the generated SCSS, JavaScript, and asset structure.

The file structure and theme configuration match the output of `theme:create` in **Shopware 6.7.16.0**. The established `Academy\AcademyTheme` PHP namespace is preserved so existing installations keep the same plugin identity.

This reference state intentionally contains no visible Storefront customization. Configurable styling and SCSS overrides are introduced in later learning units.

## Install and Assign

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

Run only one command variant. In the interactive `theme:change` command, select `AcademyTheme` and then the Storefront sales channel that should use it.

## Verify the Reference State

Verify two separate states in the Shopware Administration:

- Under **Extensions > My extensions > Themes**, `AcademyTheme` is installed and active.
- Under **Sales Channels > Storefront > Theme**, `AcademyTheme` is assigned to the Storefront sales channel.

The Storefront may still look unchanged. The theme is ready to use, but this reference state does not add visible styling.

Installation, activation, and Sales Channel assignment are stored in Shopware. They are not part of the Git tag.

## License

MIT License.

You may use this plugin in commercial and professional projects.
It is provided as an educational example and comes without a warranty and without support.

## Contributing

This plugin is part of the Shopware Academy curriculum.
