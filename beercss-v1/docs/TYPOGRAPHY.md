## Typography

### Display and Headline

size: 'small', 'medium', 'large'

**Default CSS elements**
size: 'medium'

Rule: The default CSS elements do not need to be added to the 'class'

#### Default examples

```html
<h1>Display</h1>
Display
<h2>Display</h2>
Display
<h3>Display</h3>
Headline
<h4>Headline</h4>
Headline
<h5>Headline</h5>
Headline
<h6>Headline</h6>
```

#### Custom examples

Can use: 'small' or 'large'

```html
<h1 class="large">Display</h1>
Display
<h2 class="large">Display</h2>
Display
<h3 class="large">Display</h3>
Headline
<h4 class="large">Headline</h4>
Headline
<h5 class="large">Headline</h5>
Headline
<h6 class="large">Headline</h6>
```

### Formatting

```html
link
<a class="link">link</a>

italic

<p class="italic">italic</p>

bold

<p class="bold">bold</p>

underline

<p class="underline">underline</p>

overline

<p class="overline">overline</p>

upper

<p class="upper">upper</p>

lower

<p class="lower">lower</p>

capitalize

<p class="capitalize">capitalize</p>

small-text

<p class="small-text">small-text</p>

medium-text

<p class="medium-text">medium-text</p>

large-text

<p class="large-text">large-text</p>

code

<code>code</code>

emphasized

<em>emphasized</em>

strong

<strong>strong</strong>

bold

<b>bold</b>
```

### Line spacing

line space: 'no-line', 'tiny-line', 'small-line', 'medium-line', 'large-line', 'extra-line'

**Default CSS elements**
line space: 'small-line'

Rule: The default CSS elements do not need to be added to the 'class'

#### Default example

```html
<div>
  <h5>Title</h5>
  <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
</div>
```

#### Custom example

Can use: 'no-line' or 'tiny-line' or 'medium-line' or 'large-line' or 'extra-line'

```html
<div class="large-line">
  <h5>Title</h5>
  <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
</div>
```

### Blockquote, pre and code

#### Examples

```html
<blockquote>First line.
  <br>Second line.
  <br>Third line.
</blockquote>
```

```html
<pre>First line.
Second line.
Third line.</pre>
```

```html
<pre>
  <code>// This logs a message to the console
console.log('Hello, world!')</code>
</pre>
```

```html
<p>The function
  <code>console.log()</code> prints a log message on console
</p>
```
