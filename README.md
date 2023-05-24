# Add-a-Video-on-Slider-Any-Theme-In-Shopify
Add a Video on any theme in your Shopify Store (any-theme)


<-- Create a Section on Shopify and paste the code under Slider Section, Under main <div> --> 
  
{%- if block.settings.video_link != blank -%}
<div class="fullscreen-video-wrap">
<video class="video-js" loop autoplay preload="none" muted playsinline 

poster="https:{{ block.settings.video_image | img_url: 'master' }}">

<source src="{{ block.settings.video_link }}" type="video/mp4">
</video>
</div>
{% endif %}

<-- Add a CSS in your existing Section using following code -->
  
<style>
  video{
    height: 100%;
  width: 100%;
  object-fit: cover;
  }
.videoBackground {
height: 100%;
position: relative;
}

.videoBackground .fullscreen-video-wrap {
position: absolute;
top: 0;
left: 0;
min-width: 100%;
width: 100%;
height: 100%;
overflow: hidden;

}

.videoBackground .fullscreen-video-wrap .video-js {
position: absolute;
top: 0;
left: 0;
min-height: 100%;
min-width: 100%;
width: 100%;
height: 100%;
object-fit: cover;
}

.videoBackground .fullscreen-video-wrap video {
min-height: 100%;
min-width: 100%;
object-fit: cover;
}

.videoBackground .videoBox {
display: flex;
align-items: center;
justify-content: flex-end;
flex-direction: column;
padding: 100px 20px 80px;
background-size: cover;
background-position: center;
background-repeat: no-repeat;
min-height: 500px;
max-height: 800px;
height: calc(100vh - 165px);
position: relative;

}
</style>  
  
  
<-- Add a JSON Code for show a option in your Slider -->

  {
"type": "url",
"id": "video_link",
"label": {
"en": "Video link developed By ZEE"
}
},
  
NOTE: add this properly if you want to show this into the Blocs, so you want in: Example: 
"blocks": [
    {
      "type": "slide",
      "name": "Slide",
      "settings": [
          {

And if you want to show this in your section so follow this: 
{
  "name": "Slideshow",
  "class": "slideshow--section",
  "settings": [

Add Under the Settings: if you don't understand where can i paste these code: You can contact me,...
