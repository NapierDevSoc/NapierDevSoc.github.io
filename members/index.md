---
layout: page
title: Members
navTab: Members
weight: 40
---

## GitHub
<div id="members" class="row"></div>

<script>
function defer(method) {
  if (window.$)
    method();
  else
    setTimeout(function() { defer(method) }, 50);
}

defer(function () {
  // Grab the list of members
  $.ajax("members-list.json", {
    dataType: "json"
  }).done(function(members) {

    // Loop through each member in the list
    $.each( members, function( i, name ) {

      // Fetch the member's info
      $.ajax("https://api.github.com/users/"+name, {
        dataType: "json"
      }).done(function(member) {

        // $img is used to contain the member image and name
        $img = $('<div class="col-md-3" style="margin-bottom:2em"></div>');

        // Add the image
        $( '<img>' )
          .attr( "src", member.avatar_url )
          .appendTo( $img )
          .addClass('img-thumbnail')
          .css('width', '100%');

        // Add the Name
        if (member.name)
          $img.append('<center><a href='+member.html_url+'>'+member.name+'</a></center>');
        else
          $img.append('<center><a href='+member.html_url+'>'+member.login+'</a></center>');
		  
        // Add the member ($img) to the members div
        $img.appendTo( '#members' );
      });
    });

  });
});
</script>
