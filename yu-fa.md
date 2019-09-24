# 语法

## 语法

### Hello, Ruby

```text
  #!/usr/bin/ruby -w

  puts "Hello, Ruby!";
```

这是一个简单的`ruby`程序。它的文件扩展名是`rb`,现在我们保存到文件中，取名为`test.rb`。

现在我们运行这个程序，如下

```text
$ ruby test.rb
```

结果

```text
Hello, Ruby!
```

这就是一个简单的`ruby`程序。

### Ruby中的行尾

> Ruby 把分号和换行符解释为语句的结尾。但是，如果 Ruby 在行尾遇到运算符，比如 +、- 或反斜杠，它们表示一个语句的延续。
>
> \`\`\`

> ## \#!/usr/bin/ruby -w

puts "这是一段话……";

```text
执行结果为
```

这是一段话……

```text

```

## !/usr/bin/ruby -w

puts "这是一段话……";

"结束了吗？"

```text
上述代码为在一段代码在使用`；`号结尾时另起一行写了一段文字，下面是它执行的结果
```

warning: possibly useless use of a literal in void context

```text
从上面的例子可以得出`ruby`是不支持这种语法的，接下来使用正确的语法
```

## !/usr/bin/ruby -w

puts "这是一段话……"+

"结束了吗？"

```text
执行结果
```

这是一段话结束了吗？

```text
## Ruby中的多行字符串
在 << 之后，可以指定一个字符串或标识符来终止字符串，且当前行之后直到终止符为止的所有行是字符串的值。
请注意<< 和终止符之间必须没有空格。
```

## !/usr/bin/ruby -w

print &lt;&lt;EOF 这是第一种方式创建here document 。 多行字符串。 EOF

print &lt;&lt;"EOF"; \# 与上面相同 这是第二种方式创建here document 。 多行字符串。 EOF

print &lt;&lt;`EOC` \# 执行命令 echo hi there echo lo there EOC

print &lt;&lt;"foo", &lt;&lt;"bar" \# 您可以把它们进行堆叠 I said foo. foo I said bar. bar

```text
运行后的结果：
```

这是第一种方式创建here document 。 多行字符串。 这是第二种方式创建here document 。 多行字符串。 hi there lo there I said foo. I said bar.

```text
## Ruby BEGIN 语句
```

BEGIN { …… }

```text
>BEGIN 模块中的代码将会被最早调用
```

## !/usr/bin/ruby

puts "这是主 Ruby 程序"

BEGIN { puts "初始化 Ruby 程序" }

```text
这将产生以下结果：
```

初始化 Ruby 程序 这是主 Ruby 程序

```text
虽然`BEGIN`语句写在最下面，但还是先执行的。
## Ruby END 语句
```

END { code }

```text
> END模块中的代码将会在程序的结尾被调用
```

## !/usr/bin/ruby

puts "这是主 Ruby 程序"

END { puts "停止 Ruby 程序" } BEGIN { puts "初始化 Ruby 程序" }

```text
这将产生以下结果：
```

初始化 Ruby 程序 这是主 Ruby 程序 停止 Ruby 程序

```````` END\`模块中的代码最后执行

