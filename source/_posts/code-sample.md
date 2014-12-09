title: Code Sample
date: 2014-12-01 12:28:52
tags:
- hexo
- tutorial
toc: true
---

Demos various syntax highlighting.

<!-- more -->

## C++

```cpp
#include <iostream>
 
int main()
{
     std::cout << "Hello world!\n";
     return 0;
}
```

## Java

```java
package java;

public class Java {
  public static void main(String[] argv) {
    String string = "Hello";
    System.out.println(string + " Java");
  }
}
```

## JavaScript

```javascript
function foo() {
    console.log('Hello Javascript!');
}
```

## Go

```go
import "fmt"
 
func main() {
    fmt.Println("Go Go, World!")
}

```

## CSS
```css
.article-entry .gist {
  margin: 0 -20px;
  border-style: solid;
  border-color: #ddd;
  border-width: 1px 0;
  background: #2d2d2d;
  padding: 15px 20px 15px 0;
}
```

## Gist

{% gist 7071963 %}
