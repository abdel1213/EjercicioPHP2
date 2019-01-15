<!DOCTYPE html>
 <head><title>Product Cost Calculator</title></head>
<body>
 <?php 
  // Get the values from the $_POST array:
 $price = $_POST['price'];
 $quantity = $_POST['quantity'];
 $tax = $_POST['tax'];

  // Calculate the total:
  $total = $price * $quantity;

  $taxrate = $tax/100;
  $taxrate = $taxrate + 1;

  $total = $total * $taxrate;

  $monthly = $total / $payments;

  print "<div>You have selected to
    purchase:<br />
    <span class=\"number\">$quantity</span>
    widget(s) at <br />
    $<span class=\"number\">$price</span>
    price each plus a <br />
	<span class=\"number\">$tax</span>
    percent tax rate.<br />

    Divided over <span class=\"number\">
    $payments</span> monthly payments, that
    would be $<span class=\"number\">$monthly
    </span> each.</p></div>";

  ?>
 </body>
 </html>

