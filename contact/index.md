---
layout: page
title: Contact Napier Developers Society
navTab: contact
---


<form id="contact-form" action="https://fwdform.herokuapp.com/user/864acd32-5301-4e25-8df8-6ab7c02755a4" method="post">
  <div class="row">
    <div class="large-8 columns">
      <strong id="response"></strong>
    </div>
  </div>
  <div class="row">
    <div class="large-8 columns">
      <label for="name">Name</label>
      <input id="name" name="name" type="text" placeholder="John Doe" />
    </div>
  </div>
  <div class="row">
    <div class="large-8 columns">
      <label for="email">Napier Email</label>
      <input id="email" name="email" type="text" placeholder="00000000@live.napier.ac.uk" />
    </div>
  </div>
  <div class="row">
    <div class="large-8 columns">
      <label for="message">Message</label>
      <textarea id="message" name="message" placeholder="An awesome message!" rows="4"></textarea>
    </div>
  </div>
  <div class="row">
    <div class="large-8 columns">
      <button type="submit" id="send" class="small radius button">Send!</button>
    </div>
  </div>
</form>

<script>
$('#contact-form').submit(function(event) {
  // Stop the browser from submitting the form.
  event.preventDefault();

  var $name    = $(this).find('#name');
  var $email   = $(this).find('#email');
  var $message = $(this).find('#message');

  if ($name.val().length > 0 && 
      $email.val().length > 0 &&
      $message.val().length > 0) {

    // Serialize the form data.
    var formData = $.param({
      'name'    : 'NDS: ' + $name.val(),
      'email'   : $email.val(),
      'message' : $message.val()
    });

    console.log('Please ignore the XMLHttpRequest error!');
    $.ajax({
      type: 'POST',
      url: $(this).attr('action'),
      data: formData
    });
    
    $('#response').text('Message sent!');

    // Clear the fields
    $name.val('');
    $email.val('');
    $message.val('');
  } else {
      $('#response').text('Please fill out all of the fields');
  }

});

</script>