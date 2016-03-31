title: 利器
date: 2014-03-16 01:23:37
---

<table id="mainBox" width="300" border="0" cellspacing="0" cellpadding="4" class="ke-zeroborder"><tbody><tr><td colspan="2" align="center"><strong>SHAGenerator</strong></td></tr><tr><td><span class="title">Target:</span></td><td><input type="password" name="target" id="target" /></td></tr><tr><td><span class="title">Code:</span></td><td><input type="password" name="code1" id="code1"/><input type="password" name="code2" id="code2"/></td></tr><tr><td><span class="title">Output:</span></td><td><input type="text" name="output" id="output"/></td></tr><tr><td>&nbsp;</td><td><input type="button" id="OK" name="OK" value="OK" onclick="calcHash()"/>&nbsp;&nbsp;<input type="button" id="Clear" name="Clear" value="Clear"/></td></tr></tbody></table>

<script src="/js/sha.js" type="text/javascript"></script>

<script type="text/javascript">
var hashObj;
function calcHash() {
try {
hashObj = new jsSHA(document.getElementById("target").value, "ASCII");
var tmpStr = hashObj.getHash("SHA-256", "HEX");
document.getElementById("output").value = tmpStr.substr(parseInt(document.getElementById("code1").value),parseInt(document.getElementById("code2").value));
} catch(e) {
}
}
</script>

<style type="text/css">html, body { margin:0px; padding:0px; } #mainBox { width:300px; margin:20px auto 20px; text-align:left } #target { float:left; } input { font-family:Verdana, Geneva, sans-serif; } #code1, #code2 { width:80px; border:1px solid #999; margin:0px; padding:1px; } #target, #output { width:163px; border:1px solid #999; margin:0px; padding:1px; }</style>

<div style="text-align:center;">
DBank账号：1454649618@qq.com | 987123654</div>

<div style="text-align:center;">
115账号：13693674708 | kaka123</div>