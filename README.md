# NHS Learning Hub Moodle theme
## Introduction
This is the NHS England TEL Learning Hub Moodle theme.
The theme is based on the "Boost" theme. It replaces the use of Bootstrap in the Boost theme with the use of the [NHS Design System](https://service-manual.nhs.uk/design-system) (NHS bootstrap) removing the use of Fontawesome to improve alignment with GDS and NHS Design System principles around the use of iconography.
This theme will be installed in the NHS England TEL Moodle environment as part of our work to integrate Moodle with our wider Learning Hub platform.

## Development environment
The recommended dev environment for working on this theme is as follows:
- Visual Studio Code IDE (with appropriate PHP extensions)
- Yarn
- Dart Sass

## Compiling stylesheets
To compile the Sass stylesheets in the project run:
`yarn build`
To watch the changes to .scss files for hot loading changes during dev run:
`yarn watch`

## Publishing the theme
In future, we will be implementing GitHub self-hosted runner actions to publish changes merged to this repository to our Moodle environment. Until then, we should publish the nhs-learning-hub folder directly to the Moodle environment:

**1. Prepare Your Theme Directory**
Ensure your modified theme is in a folder with the correct name (this should be the name of your theme) and contains all necessary files: config.php, version.php, theme.scss (or other CSS/Sass files), layout files, and any other assets.

**2. Place the Theme in the Moodle Theme Directory**
- Copy your theme's folder into the theme directory of your Moodle installation.
- The full path should look like this:
`moodle/theme/nhs-learning-hub/`
You can use FileZilla FTP/SFTP or directly copy the folder into the theme directory if you have access to the Moodle server.

**3. Check Permissions**
- Ensure the permissions are set correctly for the Moodle web server to access the theme files.
- Typical permissions are 755 for directories and 644 for files. You can set them using the following commands (if you have server access):
`chmod -R 755 moodle/theme/nhs-learning-hub/`

**4. Install the Theme via Moodle**
- Log in as an Admin to your Moodle site.
- Navigate to Site administration > Notifications.
Moodle will detect the new theme and prompt you to install or upgrade the site. Follow the steps to complete the installation.

**5. Activate the Theme**
Once installed, activate the theme:
- Go to Site administration > Appearance > Themes > Theme selector.
- Click "Change theme" next to the option for your current theme.
- Select the nhs-learning-hub theme from the list.
- Click "Use theme" to activate it or "Preview" to preview it.
- To preview changes in specific pages, you can also add the `?theme=nhs-learning-hub` parameter to any page in the Moodle site.

**6. Clear Moodle Cache (Optional but Recommended)**
- After installing and activating your theme, clear the Moodle cache to ensure all changes are applied correctly:
- Go to Site administration > Development > Purge caches.
- Click the "Purge all caches" button.

**7. Verify Installation**
- Check that your theme is applied properly across your Moodle site by navigating through different pages.
