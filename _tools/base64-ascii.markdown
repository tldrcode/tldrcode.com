---
layout: default
tool-name: Base64 &harr; ASCII
---
<div id="main">
  <div class="container">
    <div class="row">
      <div id="content" class="12u">
        <header>
          <h2>Base64 &harr; ASCII</h2>
        </header>
      </div>
    </div>

    <div class="row">
      <div class="6u">
        <h1 style="float: right">Base64</h1>
        <textarea type="text" id="base64" class="text-base64-ascii"></textarea>
        <br><button type="button" class="button" id="base64toascii" onclick="base64toascii()" style="width: 100%">Convert Base64 to ASCII</button>
      </div>
      <div class="6u">
        <h1>ASCII</h1>
        <textarea type="text" id="ascii" class="text-base64-ascii"></textarea>
        <br><button type="button" class="button" id="asciitobase64" onclick="asciitobase64()" style="width: 100%">Convert ASCII to Base64</button>
      </div>
    </div>

    <script language="JavaScript">
      //btoa encodes
      function base64toascii() {
        var base64string = document.getElementById('base64').value;
        document.getElementById('ascii').value = atob(base64string);
      }

      function asciitobase64() {
        var asciistring = document.getElementById('ascii').value;
        document.getElementById('base64').value = btoa(asciistring);
      }
    </script>
  </div>
</div>
