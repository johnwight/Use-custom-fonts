# Use custom fonts
Modo supports custom fonts for textual elements in your app.

Because different mobile platforms support different built-in fonts, custom fonts are the only way to ensure that the same fonts are used for text elements across all your user devices. Custom fonts can also harmonize your mobile app theme with your brand identity and lend a unique visual character to your app experience. Custom fonts can be applied to all textual elements in Modo-powered web apps, with the exception of navigation bars and menus in native iOS and Android apps. A single theme can contain multiple custom font combinations from the following:

1. [Adobe Typekit Web Fonts](https://fonts.adobe.com) 
2. [Google Fonts](https://google.com/fonts) 
3. Font files hosted from within Modo

*Note: Keep in mind that each custom font adds a typical 15-40 KB that your users will need to download.*

## How to add Adobe Typekit Fonts

To add an Adobe Fonts Typekit pack, follow these steps:

1. Go to [Adobe Typekit Fonts](https://fonts.adobe.com/?ref=tk.com) and [select](https://helpx.adobe.com/fonts/user-guide.html/fonts/using/add-fonts-website.ug.html) a pack that you want to use for your project. It is easiest to have one font family in a single pack. This includes all the weight and style variants you plan to use. For headlines, include regular and italic styles of the weight you plan to use. For body text, you will need the regular and italic styles of the normal, semi-bold (if available), and bold weights. Use a separate kit for each font family. 
2. Make sure you include the following domains in your pack settings:
    * .modolabs.com
    * .modolabs.net
    * The production domain name for your app
3. Once you’ve saved your changes, click the **Publish** button in the bottom right corner of the detail screen. 

![publish](https://user-images.githubusercontent.com/29133525/117223531-1bb8e300-adcb-11eb-9376-b882cc7d2427.png)

4. Make note of the Kit ID when it appears.
6. Click **Kits** near the top of the page to go to the [Kits](https://typekit.com/account/kits) page.
7. Find the kit you've created. The Kit ID is shown next to the kit name. It is usually a 7- or 8-character alphanumeric string. Make note of the CSS font stack. 
8. In the Adobe TypeKit Editor window, click the link **Using fonts in CSS**. This link is in the **Selectors** section near the top-left corner of the window.
9. The pop-up that appears shows the exact value that you’ll need to incude in your CSS rules. Make sure it includes **serif** or **sans-serif** as a fallback at the end. For example, ``source-sans-pro, sans-serif``as shown below. Carefully copy this value. You will need it for a subsequent step.
10. On Modo Theme Builder’s theme detail screen, click **Custom fonts**. 
11. On the **Custom Fonts screen, click the **New Custom Font** button in the top right corner of the screen.
12. Enter a unique name and ID for the new font.
13. Select **Adobe Typekit** as the source, and then click the **Add Custom Fon** button.
14. On the font editing screen, enter the Kit ID and CSS font stack from the previous steps.
15. Click the **Save & Preview** button below the sample text block. After a few seconds, the sample will refresh and will be displayed using the newly-defined custom font. If the sample preview does not look correct, double-check the Kit ID and CSS font stack against the values shown in Typekit.
16. Click the **Save** button at the top of the font editing screen to save your changes and return to the theme detail screen. From there, you can go to other aspects of the theme to apply your newly-defined custom font. For more information, see **How to apply a custom font** below.

## How to add a Google Font

To add a Google Font, follow these steps:

1. Go to Google Fonts (www.google.com/fonts) and select a font collection. It is easiest to have one font family (including all the weight and style variants you plan to use) in a single collection. Use a separate kit for each font collection.
2. Once you have a single-family collection, click the **Use** button at the bottom of the Google Fonts screen. 
3. Select the styles you plan to use. For headlines, you will need the regular and italic styles of the weight you plan to use for headlines. For body text, you will need the regular and italic styles of the normal, semi-bold (if available), and bold weights.
4. Determine the “family” parameter. To do this, in the Google Fonts **Use** screen, follow the **Add this code to your website** step, as shown below. 

  The "Standard" version of the code will share the following format: 
   ```
     <link href='https://fonts.googleapis.com/css?family=Open+Sans:400,400italic,600,
     600italic,700,700italic' rel='stylesheet' type='text/css'>
   ```
The family parameter should be everything after `family=` in the `href`. In the example above,  the `family` parameter is `Open+Sans:400,400italic,600,600italic,700,700italic`.

5. On the Google Fonts Use screen, under **Integrate the fonts into your CSS**, the exact CSS font stack for this font is shown. Make note of the CSS font stack. Be sure that it includes `sans-serif or serif as a fallback at the end. You’ll need this exact value in a subsequent step.
6. In Modo Theme Builder’s theme detail screen, click **Custom fonts**. 
7. On the Custom Fonts screen, click the **New Custom Font** button in the top-right corner.
8. Enter a unique name and ID for the new font. 
9. Select **Google Fonts** as the source, then click the **Add Custom Font** button.
10. In the font editing screen, enter the Family and CSS font stack from the previous steps.
11. Click the **Save & Preview** button below the sample text block. After a few seconds, the sample will refresh and be displayed using the newly-defined custom font. If the sample preview does not look correct, double-check the Kit ID and CSS font stack against the values shown in the Google Fonts **Use** screen.
12. Click the **Save** button at the top of the font editing screen to save your changes and to return to the theme detail screen. From there, you can go to other aspects of the theme to apply your newly defined custom font. For more information, ee the **How to apply a custom font** section below.

## How to add a custom uploaded font

To upload a custom font to your Modo theme, follow these steps:

1. On the Theme Builder detail screen, click **Custom fonts**. 
2. On the Custom Fonts screen, click the **New Custom Font** button in the top right corner of the screen.
3. Enter a unique name and ID for the new font. 
4. Select **Custom font files** as the source, and then click the **Add Custom Font** button. 
5. On the font editing screen, enter the CSS font name. This is a font-family name that should include only letters, spaces, underscores, and hyphens (e.g., my-font or my_font).
6. Enter the CSS font stack. This must be a valid comma-delimited CSS font stack. Be sure that it includes sans-serif or serif as a fallback at the end (e.g., my_font, sans-serif).
7. Upload the font file(s). A font file in WOFF format is required. TTF, EOT, and/or SVG versions can be optionally added for backwards compatibility with some older web browsers, but they are generally not needed.
8. Click the **Save & Preview** button below the sample text block. After a few seconds, the sample will refresh and be displayed using the newly-defined custom font. If the sample preview does not look correct, double-check the the CSS font name and CSS font stack you entered, and make sure you uploaded a valid WOFF file.
9. Click the **Save** button at the top of the font editing screen to save your changes and return to the theme detail screen. From there, you can go to other aspects of the theme to apply your newly defined custom font. See the “How to apply a custom font” section below.

*Note: It is the customer’s responsibility to confirm and ensure that the font(s) being used are appropriately licensed for use in websites and web applications. Modo Labs assumes no responsibility or legal liability for improper or unlicensed use of fonts or other files provided or uploaded by the customer.*

## How to apply a custom font

Once you’ve added a custom font to a theme, your theme editor will show the new font option in your drop down selections. You can use that font anywhere that a font family can be specified in the **Colors and Fonts** editing screen for that theme. See the **Colors and Fonts** reference section for more details on where you can specify fonts in the theme.

*Note: You can also use custom fonts when creating or editing Publisher screens. In these screens, wherever you see a pull-down select list for specifying a font family, select “Custom”. In the “Font stack” text field that appears, type or paste in the exact CSS font stack defined for that custom font – e.g., Open Sans, sans-serif.*
