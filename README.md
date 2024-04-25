<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SINFUL.LUA</title>
</head>
<body>
    <h1>SINFUL.LUA</h1>
    <button onclick="showProducts()">Products</button>
    <div id="productList" style="display: none;">
        <button onclick="redirectToPaypal('REGULAR')">Regular</button>
        <button onclick="redirectToPaypal('VIP')">VIP</button>
        <button onclick="redirectToPaypal('PREMIUM')">Premium</button>
    </div>

    <script>
        function showProducts() {
            var productList = document.getElementById("productList");
            if (productList.style.display === "none") {
                productList.style.display = "block";
            } else {
                productList.style.display = "none";
            }
        }

        function redirectToPaypal(product) {
            window.location.href = "https://paypal.me/LaptHim?&item_name=" + product;
        }
    </script>
</body>
</html>
