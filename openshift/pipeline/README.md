This directory contains a Jenkinsfile which can be used to build
nodejs-ex using an OpenShift build pipeline.

To do this, run:

Welcome to Fire Fighers
html>
<head>
<title>TravelBooking</title>
<meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"></script>
</head>
<body>
<div class="container-fluid" style="background-color: #333333; padding: 50px;">
  <h1 style="color: #ffffff;">TravelBooking</h1>
  <html>
<head>
<title>TravelBooking</title>
<meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"></script>
</head>
<body>
<div class="container-fluid" style="background-color: #333333; padding: 50px;">
  <h1 style="color: #ffffff;">TravelBooking</h1>
</div>
<div class="container-fluid">
<div class="row" style="padding: 50px;">
  <div class="col-sm-4" style="padding-top: 5%;">
    <label for="lname">Source:</label>
    <input id="source" type="date" name="Source" class="form-control form-control-lg">
  </div>
  <div class="col-sm-4" style="margin: auto; padding-top: 5%;">
    <img src="bus.png" style="margin-left: auto; margin-right: auto; display: block;" width="60%" alt="some image here">
  </div>
  <div class="col-sm-4" style="padding-top: 5%;">
    <label for="lname">Destination:</label>
    <input id="destination" type="date" name="Source" class="form-control form-control-lg">
  </div>
</div>
</div>
<div class="container-fluid" style="padding: 50px;">
  <h1>Passenger Information:</h1>
  <form action="/action_page.php">
  <div class="form-group">
    <label for="name">First name:</label>
    <input type="text" class="form-control" placeholder="Enter your first name" id="fname">
  </div>
  <div class="form-group">
    <label for="lname">Last name:</label>
    <input type="text" class="form-control" placeholder="Enter your last name" id="lname">
  </div>
  <div class="form-group">
    <label for="email">Email address:</label>
    <input type="email" class="form-control" placeholder="Enter your email" id="email">
  </div>
  <div class="form-group">
    <label for="pwd">Contact number:</label>
    <input type="number" maxlength="10" class="form-control" placeholder="Enter your contact number" id="pwd">
  </div>
  <div class="form-group form-check">
    <label class="form-check-label">
      <input class="form-check-input" type="checkbox"> Remember me
    </label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
</div>
</body>
</html>
```bash
# create the nodejs example as usual
oc new-app https://github.com/sclorg/nodejs-ex

# now create the pipeline build controller from the openshift/pipeline
# subdirectory
oc new-app https://github.com/sclorg/nodejs-ex \
  --context-dir=openshift/pipeline --name nodejs-ex-pipeline
```
