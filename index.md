---
---
{% include header.html %}

<div class="text-center">
	<div class="container">
	  <div class="row">
		<div class="col-12">
			<div class="jumbotron">
			  <div class="container">
				<h1 class="display-4">Welcome to our website!</h1>
				<p class="lead">Our news section is now update dynamically to provide you what you need</p>
			  </div>
			</div>
		  </div>
		</div>
	  </div>
	</div>
  <div class="py-3">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h1 class="display-4">News</h1>
        </div>
      </div>
      <div class="row">
        <div class="col-md-12">
          <div id="ann" class="lead" style="font-weight: 400">
            <p>Loading announcements...</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="py-3">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h1 class="display-4">Welcome</h1>
          <p class="lead">MTA is a non-profit after-school tutoring body set for students to develop literacy and cultural skills, provide tutoring in reading, math, and science to achieve grade-level proficiency, and to impart love, sense of belonging, and self esteem.</p>
        </div>
      </div>
    </div>
  </div>
  <div class="py-3">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h1 class="display-4">Office Hours</h1>
        </div>
      </div>
      <div class="row">
        <div class="col-md-12">
          <table class="table">
            <thead> </thead>
            <tbody>
              <tr>
                <td>Monday</td>
                <td>5 p.m. - 7 p.m.</td>
              </tr>
              <tr>
                <td>Tuesday</td>
                <td>5 p.m. - 7 p.m.</td>
              </tr>
              <tr>
                <td>Wednesday</td>
                <td>5 p.m. - 7 p.m.</td>
              </tr>
              <tr>
                <td>Thursday</td>
                <td>5 p.m. - 7 p.m.</td>
              </tr>
              <tr>
                <td>Friday</td>
                <td>5 p.m. - 7 p.m.</td>
              </tr>
              <tr>
                <td>Saturday</td>
                <td>3 p.m. - 5 p.m.</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>

<script src="papaparse.js"></script>
  <script>
    Papa.parse("https://cors-anywhere.herokuapp.com/https://docs.google.com/spreadsheets/d/e/2PACX-1vQZloUV6KYVSmI901dUpeFpq8A0N1M1JGGJhJIKLOuSStBSED4sIbrAO4cRbb2zRYO4RfI_mVKBVMhq/pub?gid=0&single=true&output=csv", {
      download: true,
      complete: function(results, file) {
        set(results);
      }
    });
    function set(data){
      ann.innerHTML = data["data"][0];
    }
    // 	$(document).ready(function(){
		// $(".ann").html(ann);
		// if(ann.trim() == ""){
		// 	$(".ann").html("No news today!");
		// }
		// });
  </script>
{% include footer.html %}
