 <script src="https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js"></script>
    <script>
        function qrgen(prefix){
            var medium = "";
            var mediumText = prefix + document.getElementById("qrtext").value;
            clearBox('qrcode');
                new QRCode(document.getElementById("qrcode"), mediumText);
        }
        function clearBox(elementID)
        {
            document.getElementById(elementID).innerHTML = "";
        }

    </script>
    <script>
