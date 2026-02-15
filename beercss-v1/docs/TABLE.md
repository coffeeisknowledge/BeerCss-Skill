## Table

align: 'left-align', 'center-align', 'right-align'
space: 'no-space', 'small-space', 'medium-space', 'large-space'

**Default CSS elements**
align: 'left-align'
space: 'small-space'

Rule: The default CSS elements do not need to be added to the 'class'

### Default Examples

```html
<table>
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer</th>
      <th>Footer</th>
      <th>Footer</th>
    </tr>
  </tfoot>
</table>
```

```html
<table class="stripes">
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer</th>
      <th>Footer</th>
      <th>Footer</th>
    </tr>
  </tfoot>
</table>
```

```html
<table class="border">
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer</th>
      <th>Footer</th>
      <th>Footer</th>
    </tr>
  </tfoot>
</table>
```

```html
<div class="small-height scroll surface">
  <table class="border">
    <thead class="fixed">
      <tr>
        <th>Header</th>
        <th>Header</th>
        <th>Header</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
    </tbody>
    <tfoot class="fixed">
      <tr>
        <th>Footer</th>
        <th>Footer</th>
        <th>Footer</th>
      </tr>
    </tfoot>
  </table>
</div>
```

### Custom Examples

Can use for align:
- 'center-align'
- 'right-align'

Can use for space:
- 'no-space'
- 'medium-space'
- 'large-space'

```html
<table class="center-align large-space">
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer</th>
      <th>Footer</th>
      <th>Footer</th>
    </tr>
  </tfoot>
</table>
```

```html
<table class="stripes center-align large-space">
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer</th>
      <th>Footer</th>
      <th>Footer</th>
    </tr>
  </tfoot>
</table>
```

```html
<table class="border center-align large-space">
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer</th>
      <th>Footer</th>
      <th>Footer</th>
    </tr>
  </tfoot>
</table>
```

```html
<div class="small-height scroll surface">
  <table class="border center-align large-space">
    <thead class="fixed">
      <tr>
        <th>Header</th>
        <th>Header</th>
        <th>Header</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
    </tbody>
    <tfoot class="fixed">
      <tr>
        <th>Footer</th>
        <th>Footer</th>
        <th>Footer</th>
      </tr>
    </tfoot>
  </table>
</div>
```
