---
layout: default
title: Смета
published: true
---

<style>
	iframe {
	  width: 100%;
	  height: 100%;
	}
</style>
<script>
  function checkFrame(iframe) {
    if (!iframe || !iframe.contentDocument || !iframe.contentDocument.location) {
      this.outterHTML = '<h3>You are not allowed to view this content :(</h3>';
    }
  }
</script>

<iframe src="https://docs.google.com/document/d/19Aw1LKBVF_6qHKFTxOW2RrAqu6rXeDzrGwhULjJflwE/preview" onload="checkFrame(this)"></iframe>
