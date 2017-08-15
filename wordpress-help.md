roots/bedrock  
deployhq  
wp migrate pro  
wp duplicator https://wordpress.org/plugins/duplicator/ 

## Upload custom fonts
- Install Font Organizer  
- to enable any font name and not keep it to 20 characters:  
  in wp-content/plugins/font-organizer/general-settings.php  
  remove maxlength="20" on line 46
- issue with font precedence... -> prefer a child theme where custom fonts are uploaded

## Upgrade a theme manually
- make sure to add the version number to the new theme folder so that it doesn't conflict with the previous one

## Plugins
- Yoast SEO  
- Divi theme + builder  
- WP Rocket for caching  
- Font organizer for custom fonts: but some precedence rules issue (see above)  
- 
