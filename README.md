# Handyman-App-Email
# Having issues with get my app (ionic framework, angular,js, cordova) to send an email with attachment.
# Please see below for the block of code used in the app.

$scope.sendEmail = function(){
       var bodyText = "<h2>See attached invoice for pricing</h2>";
       window.plugin.email.open({
           to: ["aj.rogers@spectregames.com"],
           attachments: ['file://img/test.png'], //only works if the file is file://index.html
           subject: "Split-Second Quotes Invoice",
           body: bodyText,
           isHtml: true,
       }, function (){
           console.log('email view dismissed');
       },
       this);
       }
