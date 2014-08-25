---
layout: page
title: Contact Napier Developers Society
navTab: contact
---


<form action="http://nds.herokuapp.com/" method="post">
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
      <button id="send" class="small radius button">Send!</button>
    </div>
  </div>
</form>
