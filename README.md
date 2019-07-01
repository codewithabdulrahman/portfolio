# portfolio
just a links of portfolio

https://grokonez.com/frontend/angular/angular-6/angular-6-form-validation-example-template-driven-forms

<h1>abdul.rahman6340@gmail.com</h1>

<b>Wordpress Work</b>

http://imhpackaging.com/  <br>
http://www.wegrindglobal.com/  <br>
https://websitesample.name/  <br>
http://www.sajjadtextile.com/   <br>


<b>Magento Work</b>

https://dev.itechdevices.co.uk/    <br>
https://reliancesolution.co.uk/    <br>
http://javinci.com/en/    <br>

---Catagory page---
<?php $page_object = get_queried_object(); ?>
<?php $categoryID= $page_object->cat_ID; ?>

<?php query_posts("cat=$categoryID"); ?>
<?php if ( have_posts() ) : while ( have_posts() ) : the_post(); ?>
    <li><a href="<?php the_permalink() ?>" rel="bookmark"><?php the_title(); ?></a></li>
<?php endwhile; endif; ?>




----Single.php----
<?php if (have_posts()) : while (have_posts()) : the_post(); ?>

	<?php the_title(); ?>
	<?php the_content(); ?>
	<?php echo get_the_date(); ?>

<?php endwhile; ?>
<?php endif; ?>
