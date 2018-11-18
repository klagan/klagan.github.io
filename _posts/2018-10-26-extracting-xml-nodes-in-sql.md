---
published: true
tags: sql
---
I always run into this issue where I want to extract values or nodes from xml stored in a database. 

Im not saying this is a production solution, but when trouble shooting it is useful to be able to extract snippets out data from samples of information.

```
DECLARE @xml XML
SET @xml = '<root><name>Angry Ape</name><addr>Congo</addr></root>'
SELECT @xml.query('(root/name)')
SELECT @xml.value('(root/name)[1]', 'NVARCHAR(MAX)')
```

Hooray!


({{ site.baseurl }}/_assets/extracting-xml-sql.png)
