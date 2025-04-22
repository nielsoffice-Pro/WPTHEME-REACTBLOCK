# WPTHEME-REACTBLOCK
WordPress Theming block react JS


```
STRUCTURE

  > Yout Theme
    > assets
    > parts
    > patterns
    > styles
    > templates
    > functions.php
    > screenshot.png
    > theme.json

   Hierarchy
    > patterns
        create file in patterns
        footer.php
        /**
         * Title: Footer
         * Slug: twentytwentyfive/footer
         * Categories: footer
         * Block Types: core/template-part/footer
         * Description: Footer columns with logo, title, tagline and links.
         *
         * @package WordPress
         * @subpackage Twenty_Twenty_Five
         * @since Twenty Twenty-Five 1.0
         */
         
        | > Parts
             import file from pattern to part static html
             <!-- wp:pattern {"slug":"youthemename/patternname"} /-->
             ex. <!-- wp:pattern {"slug":"twentytwentyfive/footer"} /-->
             footer.html

              | > templates
                    Implement part to templates
                    ex. index.html

                    // header.html from PART 
                    <!-- wp:template-part {"slug":"header"} /-->

                    // this template also from part, it is a group !
                    <!-- wp:group {"tagName":"main","style":{"spacing":{"margin":{"top":"var:preset|spacing|60"}}},"layout":{"type":"constrained"}} -->
                    <main class="wp-block-group" style="margin-top:var(--wp--preset--spacing--60)">
                    	<!-- wp:pattern {"slug":"twentytwentyfive/hidden-blog-heading"} /-->
                    	<!-- wp:pattern {"slug":"twentytwentyfive/template-query-loop"} /-->
                    </main>
                    <!-- /wp:group -->

                    // footer.html from PART 
                    <!-- wp:template-part {"slug":"footer"} /-->

                   
```

Helpful tip: 

WP Plugin Block Development link: https://github.com/nielsoffice-Pro/WPBlockExtendDevelopment
