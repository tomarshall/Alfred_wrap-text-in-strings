# alfred-wrap-text
This Alfred workflow wraps whatever text is highlighted on your screen in pre-specified text strings. By default, this workflow will wrap the highlighted text in double carets (i.e. "^^"), but you can very easily change what text to add right before and after your highlighted text by simply editing the code to replace the `'^^'`'s on each side of `argv` with whatever text you want (making sure that whatever text you want to add is also surrounded by quotation marks).

This is how the Ruby code that powers workflow looks "out of the box":
```ruby
print ARGV.map{ |argv|'^^' + argv + '^^' }.join
```

If I wanted to change the workflow to wrap a piece of text—like "hello, world", for example—such that it came out "Well, hello, world!", all I would have to do is edit the code to look like this:

```ruby
print ARGV.map{ |argv|'Well, ' + argv + '!' }.join
```
