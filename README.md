<!DOCTYPE html>
<html>
<head>
<style>
.flex-container {
  display: flex;
  flex-wrap: nowrap;
  max-width:150px;
}

.flex-container > input {
  -webkit-flex: 1; /* Safari 6.1+ */
    -ms-flex: 1; /* IE 10 */ 
    flex: 1;
    width:25px;
  border: 0;
  outline: 0;
  text-align: right;
}
</style>
</head>
<body>
<h1>Flexible Boxes</h1>

<div class="flex-container">
  <input type="password" maxlength=1 id="1" onkeyup="moveOnMax(this,'a')" placeholder='*' />
  <input type="password" maxlength=1 id="a" onkeyup="moveOnMax(this,'b')" placeholder='*'/>
<input type="password" maxlength=1 id="b" onkeyup="moveOnMax(this,'c')" placeholder='*'/>
<input type="password" maxlength=1 id="c" onkeyup="moveOnMax(this,'d')" placeholder='*'/>
<input type="password" maxlength=1 id="d" onkeyup="moveOnMax(this,'e')" placeholder='*'/>
<input type="password" maxlength=1 id="e" placeholder='*' />
</div>






</body>
</html>
<script>
moveOnMax =function (field, nextFieldID) {
    if (field.value.length == 1) {
        document.getElementById(nextFieldID).focus();
    }
}
</script>
