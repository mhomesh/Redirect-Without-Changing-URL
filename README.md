# Redirect-Without-Changing-URL
Redirect Without Changing URL using .htaccess
<IfModule mod_rewrite.c>
	RewriteEngine on

  RewriteRule ^about-us$ aboutus.php

  # Rewrite URLs of the form 'x' to the form 'index.php?q=x'.
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_FILENAME} !-d
  RewriteCond %{REQUEST_URI} !=/favicon.ico
  RewriteRule ^(.*)$ index.php?q=$1 [L,QSA]
</IfModule>
