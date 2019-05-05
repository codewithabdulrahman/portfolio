# portfolio
just a links of portfolio

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

//////////////////////////
echo get_theme_mod('ek_image_about_info');
echo wp_get_attachment_url(get_theme_mod('ek_image_about_info'));


// custom theme panel
function ek_register_customizer($wp_customize)
{
    $wp_customize->add_panel('ek_custom_panel', array(
        'title' => 'Custom Theme Panel',
        'description' => 'This is customizer',
        'priority' => 20,
    ));

    // Footer Section

    $wp_customize->add_section('ek_Footer_section', array(
        'title' => 'Footer_sections',
        'description' => 'Change Footer section',
        'priority' => 10,
        'panel' => 'ek_custom_panel',
    ));
    $wp_customize->add_setting('ek_contact_info', array(
        'default' => 'Ali',
        'transport' => 'refresh',
    ));
    $wp_customize->add_control( 'ek_contact_control',array(
        'title'=> 'Add Copyright info',
        'type' => 'text',
        'input_attr' =>[
            'class'=>'form-control',
        ],
        'section' => 'ek_Footer_section',
        'settings'=> 'ek_contact_info',
    ));

    // Image Section
    $wp_customize->add_section('ek_image_about', array(
        'title' => 'Footer_sections',
        'description' => 'Change Footer section',
        'priority' => 10,
        'panel' => 'ek_custom_panel',
    ));
    $wp_customize->add_setting( 'ek_image_about_info', array(
        'default' => '#000',
        'transport' => 'refresh',
    ));
    $wp_customize->add_control(new WP_Customize_Media_Control($wp_customize,'ek_bg_image',array(
     'label'=>__('Background Image','ektheme'),
     'section'=> 'ek_image_about',
     'settings'=> 'ek_image_about_info',  
     'mime_type'=>'image',
    )));
}

add_action('customize_register', 'ek_register_customizer', 10, 1);

<-------------------------------------------------------------------------------------------------------------------------->


    <div class="row" style="padding: 30px;">
        <div class="col-md-3" style="border-right:1px solid black;border-bottom:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;border-bottom:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;border-bottom:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;border-bottom:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;">
            Connecting drivers with advertisement
        </div>
        <div class="col-md-3" style="border-right:1px solid black;">
            Connecting drivers with advertisement
        </div>
    </div>
    
    <---------------------------------------------------------------------------------------------->
    
    <div class="row" style="padding: 40px;">
    <div class="col-md-2"></div>
    <div class="col-md-4">
        <?php echo do_shortcode('[wppb-login]')?>
    </div>
    <div class="col-md-4">
        <?php echo do_shortcode('[wppb-register]')?>
    </div>
    <div class="col-md-2"></div>
</div>
