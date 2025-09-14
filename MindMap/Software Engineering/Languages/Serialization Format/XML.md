- **Extensible Markup Language** is a serialization format language

- It's HTML-like where tags have names as key for data and content as data.
- The tags describe what the data means
```xml
<title> Atack On Titans </title>
<price> 49.99 </price>
```

- It can nest tags to represent hierarchical structure of data.
```xml
<film>
	<title> ... </title>
	<price> ... </price>
</film>
```

- Before [[JSON]] became popular, XML was the main format to transfer data between web servers and applications.
- Cons:
- XML is often verbose (it uses many tags and takes more space).