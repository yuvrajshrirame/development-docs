# Markdown Crash Course

> Learnt from Traversy Media on YouTube
> 

### What is Markdown?

- Lightweight markup language with a plain text formatting syntax.
- Can be converted in HTML/XHTML and other formats.
- It’s main purpose is readability and ease of use.
- Characters and punctuation marks are used to format text.

### What is it used for?

- GitHub Readme Files.
- Blog Posts & Forums.
- Used in many static sites generator.

### What can be done using Markdown?

- Headings
- Emphasis
- Bold
- Lists
- Links
- Code Blocks
- Images
- Block Quotes
- Horizontal Rules

### Markdown Editors

- Code Editors (VS Code, Atom)
- Markpad
- Haroopad
- Typora

### Cheat Sheet

```markdown
<!-- Open Markdown Preview Present After Run Button on Top Right Corner (In VS Code) -->

<!-- Headings -->
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

<!-- Italics -->
This text is *Italic*
OR
This text is _Italic_

<!-- Strong -->
This text is **Bold**
OR
This text is __Bold__

<!-- Line Breaks -->
<!-- WAY-01: Add 2 Spaces at the End -->
<!-- Soft Breaks -->
Cat is running behind the Mouse  
Cat is running behind the Mouse
<!-- WAY-02: Hit Enter 2 Times -->
<!-- Hard Breaks -->
Cat is running behind the Mouse

Cat is running behind the Mouse

<!-- Strikethrough -->
This text is ~~deleted~~

<!-- Horizontal Rule -->
---
OR
___

<!-- To Show Special Characters -->
This text is \*Italic\*

<!-- Block Quotes -->
> This is a Block Quote
>
> _- John Doe_

<!-- Links -->
[Google](https://google.com)

Title Appears in the Below Link on Hovering

[Google](https://google.com "Open Google.com")

<!-- Lists -->
<!-- UL -->
* Item 1
* Item 2
* Item 3
* Item 4
    * Item 4.1
    * Item 4.2
<!-- OL -->
1. Item 1
1. Item 2
1. Item 3
1. Item 4
    1. Item 4.1
    1. Item 4.2

<!-- Inline Code Block -->
`<html> This is HTML Tag </html>`

<!-- Images -->
![Image](https://pwskills.com/images/PWSkills-main.png)

<!-- GitHub Markdown -->

<!-- Code Blocks -->
```bash
npm install

npm start
```

```javascript
function add(num1, num2){
    return num1 + num2;
}
```

<!-- Tables -->
| Name     | Email          |
|----------|----------------|
| John Doe | john@gmail.com |
| John Doe | john@gmail.com |

<!-- Tasklists -->
<!-- It will show only on GitHub Readme, not here, because Tasklist is GitHub Specific -->

* [x] Task Done
* [ ] Task Incomplete
```