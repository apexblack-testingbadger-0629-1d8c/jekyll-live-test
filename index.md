---
layout: null
---
# RCE Test V2
Canary: {{ site.data.evil.canary | default: "FAIL" }}
Erb: {{ site.data.evil.erb | default: "FAIL" }}
Cmd: {{ site.data.evil.cmd | default: "FAIL" }}
File: {{ site.data.evil.file_read | default: "FAIL" }}
