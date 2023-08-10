# Clean-Code-Go
🛁 Clean Code concepts and tools adapted for Go [WORK IN PROGRESS] 

## Table of Contents

1. [Introduction](#introduction)
2. [variables](#variables)

## Introduction

![Humorous image of software quality estimation as a count of how many expletives
you shout when reading code](https://www.osnews.com/images/comics/wtfm.jpg)

Software engineering principles, from Robert C. Martin's book
[*Clean
Code*](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
, adapted for Go. This is not a style guide. It's a guide to producing
readable, reusable, and refactorable software in Go.

Not every principle herein has to be strictly followed, and even fewer will be
universally agreed upon. These are guidelines and nothing more, but they are
ones codified over many years of collective experience by the authors of *Clean
Code*.

Our craft of software engineering is just a bit over 50 years old, and we are still learning a lot. When software architecture is as old as architecture itself, maybe then we will have harder rules to follow. For now, let these guidelines serve as a touchstone by which to assess the quality of the JavaScript code that you and your team produce.

One more thing: knowing these won't immediately make you a better software developer, and working with them for many years doesn't mean you won't make mistakes. Every piece of code starts as a first draft, like wet clay getting shaped into its final form. Finally, we chisel away the imperfections when we review it with our peers. Don't beat yourself up for first drafts that need improvement. Beat up the code instead!

Adapted from 
from [clean-code-javascript](https://github.com/ryanmcdermott/clean-code-javascript),
[clean-code-python](https://github.com/zedr/clean-code-python),
and [clean-code-ruby](https://github.com/uohzxela/clean-code-ruby)

## **Variables**

### Use meaningful and pronounceable variable names

**Bad:**

```Go
import (
	"fmt"
	"time"
)

yyyymdstr := fmt.Sprintf("%d/%d/%d", time.Now().Year(), time.Now().Month(), time.Now().Day())
```

**Good:**

```Go
import (
	"fmt"
	"time"
)

currentDate := fmt.Sprintf("%d/%d/%d", time.Now().Year(), time.Now().Month(), time.Now().Day())
```

**[⬆ back to top](#table-of-contents)**


### Use the same vocabulary for the same type of variable

**Bad:**

```Go
getUserInfo()
getClientData()
getCustomerRecord()
```

**Good:**

```Go
getUser()
```

**[⬆ back to top](#table-of-contents)**

### Use searchable names

We will read more code than we will ever write. It's important that the code we do write is readable and searchable. By not naming variables that end up being meaningful for understanding our program, we hurt our readers. Make your names searchable.

**Bad:**

```Go
```

**Good:**

```Go
```

**[⬆ back to top](#table-of-contents)**

### Use explanatory variables

**Bad:**
```Go
```

**Good:**
```Go
```

**[⬆ back to top](#table-of-contents)**


### Avoid Mental Mapping 
