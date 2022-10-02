#  MarkDown Tags

# Title H1
```
# Title H1 
```
## Title H2
```
## Title H2
```
### Title H3
```
### Title H3
```
#### Title H4
```
#### Title H4
```
##### Title H5
```
#### Title H5
```
###### Title H6
```
##### Title H6
```
Don't exist H7
```
###### Title H7 - Don't exist
```
Another type of Title H1
=
```
Another type of Title H1
=
```
Another type of Title H2
-
```
Another type of Title H2
-
```
---
_ITALIC_
```
_ITALIC_
```
Another type of *ITALIC*
```
*ITALIC*
```
**BOLD**
```
**BOLD**
```
Another type of __BOLD__
```
__BOLD__
```
---
# LINKS

### Text with URL Link
[How-To](https://github.com/PhilipMello/how-to)
```
[How-To](https://github.com/PhilipMello/how-to)
```
### Text with URL Link + Title
[How-To](https://github.com/PhilipMello/how-to "How-To (HTML, CSS, MarkDown, PHP, JS, Java, Python)")
```
[How-To](https://github.com/PhilipMello/how-to "How-To (HTML, CSS, MarkDown, PHP, JS, Java, Python)")
```
### Simple URL Link
<https://github.com/PhilipMello/how-to>
```
<https://github.com/PhilipMello/how-to>
```
---
# QUOTES

### ONE LINE QUOTE
> QUOTE
```
> QUOTE
```
#### MULTILINE QUOTE
> QUOTE LINE 1
> QUOTE LINE 1
> QUOTE LINE 3
```
> QUOTE LINE 1
> QUOTE LINE 1
> QUOTE LINE 3
```
---
# LISTS

### UNORDERED LIST
- Apple
  - iPhone
  - iPad
  - Macbook
  - iMac
```
- Apple
  - iPhone
  - iPad
  - Macbook
  - iMac
```
### ANOTHER MODE FOR UNORDERED LIST
* Apple
  * iPhone
  * iPad
  * Macbook
  * iMac
```
* Apple
  * iPhone
  * iPad
  * Macbook
  * iMac
```
### ORDENED LIST
1. Apple
  1. iPhone
  1. iPad
  1. Macbook
  1. iMac
```
1. Apple
  1. iPhone
  1. iPad
  1. Macbook
  1. iMac
```
----
# IMAGES

### Local Images no Title
![GitHub](github-logo.png)
```
![GitHub](github-logo.png)
```

### Local Images with Title
![GitHub](github-logo.png "GitHub Logo")
```
![GitHub](github-logo.png "GitHub Logo")
```

### External Images no Title
![GitHub](https://raw.githubusercontent.com/PhilipMello/how-to/main/markdown/github-logo.png)
```
![GitHub](https://raw.githubusercontent.com/PhilipMello/how-to/main/markdown/github-logo.png)
```

### External Images with Title
![GitHub](https://raw.githubusercontent.com/PhilipMello/how-to/main/markdown/github-logo.png "GitHub Logo")
```
![GitHub](https://raw.githubusercontent.com/PhilipMello/how-to/main/markdown/github-logo.png "GitHub Logo")
```

# TABLES

### 2 Column - Default left alignment

| Products | Price |
|----------|-------|
|iPhone    |$199.00  |
|iPad      |$399.00  |
|MacBook   |$999.00  |
|iMac      |$1.399,00|

```
| Products | Price |
|----------|-------|
|iPhone    |$199.00  |
|iPad      |$399.00  |
|MacBook   |$999.00  |
|iMac      |$1.399,00|
```

### 2 Column - Right alignment

| Products | Price |
|---------:|-------:
|iPhone    |$199.00  |
|iPad      |$399.00  |
|MacBook   |$999.00  |
|iMac      |$1.399,00|

```
| Products | Price |
|---------:|-------:
|iPhone    |$199.00  |
|iPad      |$399.00  |
|MacBook   |$999.00  |
|iMac      |$1.399,00|
```

### 2 Column - Center alignment

| Products | Price |
:---------:|:------:
|iPhone    |$199.00  |
|iPad      |$399.00  |
|MacBook   |$999.00  |
|iMac      |$1.399,00|

```
| Products | Price |
:---------:|:------:
|iPhone    |$199.00  |
|iPad      |$399.00  |
|MacBook   |$999.00  |
|iMac      |$1.399,00|
```

---

# CODE TEXT UNFORMATED

### HTML

<h2>CODE HTML</h2>
<h3>CODE HTML</h3>
<h4>CODE HTML</h4>
<h5>CODE HTML</h5>

```
<h2>CODE HTML</h2>
<h3>CODE HTML</h3>
<h4>CODE HTML</h4>
<h5>CODE HTML</h5>
```

# CODE TEXT FORMATED

### HTML

```html
<h1>CODE HTML</h1>
<h2>CODE HTML</h2>
<h3>CODE HTML</h3>
<h4>CODE HTML</h4>
```

```
```html
<h1>CODE HTML</h1>
<h2>CODE HTML</h2>
<h3>CODE HTML</h3>
<h4>CODE HTML</h4>
```

### CSS

```css
<style>
.btn {
  background-color: Blue;
  border: none;
  color: white;
  padding: 12px 30px;
  cursor: pointer;
  font-size: 20px;
}
</style>
```

```
```css
<style>
.btn {
  background-color: Blue;
  border: none;
  color: white;
  padding: 12px 30px;
  cursor: pointer;
  font-size: 20px;
}
</style>
```

### PHP

```php
<?php
echo "Hello World"
>
```

```
```php
<?php
echo "Hello World"
>
```

### Java

```java
System.out.print("Hello World");
```

```
```java
System.out.print("Hello World");
```

---
# TO-DO LIST
- [ ] Got to market
- [ ] Buy food
- [ ] Rest
- [ ] Play game

```
# TO-DO LIST
- [ ] Got to market
- [ ] Buy food
- [ ] Rest
- [ ] Play game
```

---

# Variables

### Images in variables

[github_logo]: github-logo.png

![Variable Image][github_logo]

```
[github_logo]: github-logo.png

![Variable Image][github_logo]
```

### Links in variable

[github_profile]:https://github.com/PhilipMello

[GitHub Profile][github_profile]

```
[github_profile]:https://github.com/PhilipMello

[GitHub Profile][github_profile]
```