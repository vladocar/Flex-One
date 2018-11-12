<h1 align="center"> Flex One - 1 CSS Class System </h1>

<p align="center"> Flex One is CSS Layout system based on one CSS class. This class: .fluid {flex:1} </p>

<hr/>

<p>With this .fluid {flex:1} you can build entire CSS grid system. </p>

<h4>Let me show you how it works: </h4>

```shell
.main{display: flex; flex-flow: row wrap;  width: 80%; margin: 0 auto}

.fluid{flex:1}

.clear{width: 100%}
```

```shell
<div class="fluid">33,3%</div>
<div class="fluid">33,3%</div>
<div class="fluid">33,3%</div>
<div class="clear"></div>

<div class="fluid">25%</div>
<div class="fluid">25%</div>
<div class="fluid">25%</div>
<div class="fluid">25%</div>
<div class="clear"></div>
```

<p>Super simple, just add the number of columns you need. You can have infinite number of columns. Plus is fluid with natural responsiveness.</p>

<p> When you are finished add the .clear class.</p>

<p><a href="https://vladocar.github.io/Flex-One/"> Here is the demo Grid</a>

<h4>Limitations? Yes, many. </h4>

<p> One of the biggest limitation is: you must use identical size columns. You can't have 1-1-1-3 or 1-2-1 grid.

<p> We can fix these limitations by adding some CSS code:</p>

```shell
.merge2 {flex:2}
.merge3 {flex:3}
```

Now we can have this 1-1-1-3:

```shell
<div class="fluid">1</div>
<div class="fluid">1</div>
<div class="fluid">1</div>
<div class="merge3">Merge 3</div>
<div class="clear"></div>
```

<img src="1-1-1-3.png" />

<h4>What about nested columns? </h4>

<p> We can use this code for the nested columns:</p>

```shell
.nested{display: flex; flex-flow: row wrap; padding:0 !important; margin:0 !important; border: 0 !important}
```

```shell
<div class="fluid nested">
    <div class="fluid">Nested column</div>
    <div class="fluid">Nested column</div>
</div>
```
<p>Inside any fluid column we can insert any number of other fluid columns by adding the .nested class.</p>

<h4>Ok. What about gutter?</h4>

<p>The Gutter is optional. If you need it you can use something like this:</p>

```shell
.fluid,.merge2,.merge3 {margin:0 0 0 15px}

// or maybe

.fluid,.merge2,.merge3,.merge4 {padding:0 10px}
```

<h4>Some other tweaks.</h4>

<p> Here is also alternative to the .clear class:</p>


```shell
<div class="fluid"></div>
<div class="fluid"></div>
<div class="fluid"></div>
<div class="clear"></div>

// Alternative columns class:

<div class="columns">
<div class="fluid"></div>
<div class="fluid"></div>
<div class="fluid"></div>
</div>
```

<h4>Conclusion</h4>

<p> Starting with the .fluid{flex:1} class and by adding few other CSS classes we can build infinite column grid system that is fluid and responsive.
