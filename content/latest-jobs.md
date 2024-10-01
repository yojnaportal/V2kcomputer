+++
title = 'New Page'
date = "2023-10-01"
draft = false
description =""
image =""
imageBig =""
lastdate ="2024-10-20"
post-type= "latest-jobs"
Categories = []
authors = ["vikram Singh"]
avatar  = "/images/"
+++ 
{{ define "main" }}
    {{ partial "list-posts.html" . }}
    {{ partial "list-home.html" . }}
   
   
    <h1>Categories</h1>
    <ul>
    {{ range $key, $value := .Site.Taxonomies.categories }}
        <li>
            <a href="{{ "/categories/" | relLangURL }}{{ $key | urlize }}">{{ $key | title }} ({{ len $value }})</a>
        </li>
    {{ end }}
    </ul>
    
{{ end }}