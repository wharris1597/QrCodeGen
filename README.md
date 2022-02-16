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

 
 
 
 
 <div class="row gx-0 mb-5 mb-lg-0 justify-content-center">
            <div class="col-lg-6">
                <div id="qrcode"></div>
            </div>
            <div class="col-lg-6">
                <div class="bg-black text-center h-100 project">
                    <div class="d-flex h-100">
                        <div class="project-text w-100 my-auto text-center text-lg-left">

                            <h4 class="text-white">QR Code Generator</h4>
                            <p class="mb-0 text-white-50">This is a QR Code generator that demonstrates a small amount of javascript and HTML knowledge.
                            Enter some text to generate a code. IT can be a website or a secret message to a friend!</p>
                           <br />
                            <input id="qrtext" type="text" placeholder="Embedded QR Text" />
                            <br /><br />
                            <button onclick="qrgen('')">Generate Text Code</button><br /><br />
                            <div class="dropdown">
                                <button onclick="myFunction()" class="dropbtn">More Options</button>
                                <div id="myDropdown" class="dropdown-content">
                                    <button id="call" onclick="qrgen('tel:')">Call</button><br />
                                    <button id="email" onclick="qrgen('mailto:')">Email</button><br />
                                    <button id="text" onclick="qrgen('sms:')">Text</button>
                                </div>

                            </div>


                            <hr class="d-none d-lg-block mb-0 ms-0" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
