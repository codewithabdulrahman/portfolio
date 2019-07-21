# portfolio
just a links of portfolio

https://grokonez.com/frontend/angular/angular-6/angular-6-form-validation-example-template-driven-forms

<h1>abdul.rahman6340@gmail.com</h1>


{
  "require":{
    "sendgrid/sendgrid":"~7"
  }
}
-----


<?php
$curl = curl_init();

curl_setopt_array($curl, array(
    CURLOPT_URL => "https://api.sendgrid.com/v3/mail/send",
    CURLOPT_RETURNTRANSFER => true,
    CURLOPT_ENCODING => "",
    CURLOPT_MAXREDIRS => 10,
    CURLOPT_TIMEOUT => 30,
    CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
    CURLOPT_CUSTOMREQUEST => "POST",
    CURLOPT_POSTFIELDS => "{\r\n  \"personalizations\": [\r\n   
 {\r\n      \"to\": [\r\n        {\r\n          \"email\": \"devlobb@gmail.com\"\r\n       
 }\r\n      ],\r\n      \"subject\": \"Welcome to Techhawa!\"\r\n    }\r\n  ],\r\n  
\"from\": {\r\n    \"email\": \"abdul.rahman6340@gmail.com\"\r\n  },\r\n  \"content\": [\r\n    
{\r\n      \"type\": \"text/plain\",\r\n      \"value\": \"Hello, World!\"\r\n    }\r\n 
 ]\r\n}",
    CURLOPT_HTTPHEADER => array(
        "authorization: Bearer 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",
        "cache-control: no-cache",
        "content-type: application/json"
    ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
    echo "cURL Error #:" . $err;
} else {
    echo $response;
}
?>
