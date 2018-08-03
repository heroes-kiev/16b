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
  function err(a, b, c) {
  	console.log('catched e', a, b, c);
  }

  window.onerror = err;

  function checkFrame(iframe) {
    if (!iframe || !iframe.contentDocument || !iframe.contentDocument.location) {
//      iframe.outerHTML = '<h3>You are not allowed to view this content :(</h3>';
    }
  }
</script>

<iframe src="https://docs.google.com/document/d/19Aw1LKBVF_6qHKFTxOW2RrAqu6rXeDzrGwhULjJflwE/preview" onload="checkFrame(this)" onerror="err(this)" frameborder="0"></iframe>
