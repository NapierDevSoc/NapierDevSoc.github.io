---
layout: page
title:  News
navTab: News
weight: 20
---

<!-- Begin MailChimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/classic-081711.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; }
	/* Add your own MailChimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="//napierdevsoc.us9.list-manage.com/subscribe/post?u=6348bfc49a97aec46af2b102d&amp;id=85c32cc3f1" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<h2>Subscribe to our mailing list</h2>
<div class="indicates-required"><span class="asterisk">*</span> indicates required</div>
<div class="mc-field-group">
	<label for="mce-EMAIL">Email Address  <span class="asterisk">*</span>
</label>
	<input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL">
</div>
<div class="mc-field-group">
	<label for="mce-FNAME">First Name  <span class="asterisk">*</span>
</label>
	<input type="text" value="" name="FNAME" class="required" id="mce-FNAME">
</div>
<div class="mc-field-group">
	<label for="mce-LNAME">Last Name  <span class="asterisk">*</span>
</label>
	<input type="text" value="" name="LNAME" class="required" id="mce-LNAME">
</div>
	<div id="mce-responses" class="clear">
		<div class="response" id="mce-error-response" style="display:none"></div>
		<div class="response" id="mce-success-response" style="display:none"></div>
	</div>    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;"><input type="text" name="b_6348bfc49a97aec46af2b102d_85c32cc3f1" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
</form>
</div>
<script type='text/javascript' src='//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js'></script><script type='text/javascript'>(function($) {window.fnames = new Array(); window.ftypes = new Array();fnames[0]='EMAIL';ftypes[0]='email';fnames[1]='FNAME';ftypes[1]='text';fnames[2]='LNAME';ftypes[2]='text';fnames[3]='MMERGE3';ftypes[3]='text';fnames[4]='MMERGE4';ftypes[4]='text';}(jQuery));var $mcj = jQuery.noConflict(true);</script>
<!--End mc_embed_signup-->

<div class="posts">
  {% if site.categories.news %}
  {% for post in site.categories.news limit:5 %}
    <div class="post">  
      <h2>
        <a href="{{ post.url | prepend: site.baseurl }}">
          {{ post.title }}
          {% if post.category != 'minutes' %}
            <small>{{ post.date | date: "%B %-d, %Y" }}</small>
          {% endif %}
        </a>
      </h3>
      <p class="post-meta">
        Published by <a href="https://github.com/{{ post.author }}">{{ post.author }}</a>
      </p>


      <div class="content">
        {{ post.excerpt | remove: '<h2>' | remove: '</h2>' }}
      </div>
    </div>
  {% endfor %}
  {% else %}
  <p> No news items at this time, please check back soon. </p>
  {% endif %}
</div>
