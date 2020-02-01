# Mesh, a simple grid

Mesh is a simple grid that will fall-back to the old-style grid to avoid
your typical internet-explorer issues. It supports most grid functionality
and utilizes CSS margin collapsing to make the grid pad items accordingly.

If you want to learn more about grids, check out [this documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout) 
that Mozilla wrote on it. It contains the fundamentals for this grid
system too.
=======
# Mesh, a simple grid

Mesh is a simple grid that will fall-back to the old-style grid to avoid
your typical internet-explorer issues. It supports most grid functionality
and utilizes CSS margin collapsing to make the grid pad items accordingly.

If you want to learn more about grids, check out [this documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
that Mozilla wrote on it. It contains the fundamentals for this grid
system too.

Using the mesh is quite easy. To create your common product grid that you
see on most e-commerce sites these days, you can initialize it  as follows:

```html
<div class="mesh-container">
  <div class="mesh-unit-xs--col-12 mesh-unit-l--col-6 mesh-unit-xl--col-4">
    Item 1
  </div>
  <div class="mesh-unit-xs--col-12 mesh-unit-l--col-6 mesh-unit-xl--col-4">
    Item 2
  </div>
  ...
</div>
```

## Nesting meshes

You can also nest meshes. Because it utilizes margin collapsing, your grid
will always remain aligned perfectly.

```html
<div class="mesh-container">
  <div class="mesh-unit-xs--col-12 mesh-unit-l--col-6 mesh-unit-xl--col-4">
    <div class="mesh-container">
      ...
    </div>
  </div>
</div>
```

## Adding spacing between grid elements

You can also add spacing between your grid elements by adding more classes
to your grid container element:

```html
<div class="mesh-container mesh-container-xs--gap-4--x mesh-container-xs--gap-2--y">
</div>
```

## Vertically stacking elements within a grid element with perfect spacing

We also can utilize sections to unify margins within a `mesh-unit`, these
will add proper spacing between stacked elements without making the last
item overflow and misalign the mesh:

```html
<div class="mesh-container">
  <div class="mesh-unit-xs--col-12 mesh-unit-l--col-6 mesh-unit-xl--col-4">
    <div class="mesh-section-xs--gap-4">
      This element will not have any margin on the top
    </div>
    <div class="mesh-section-xs--gap-4">
      This element will have margin on the top to space the elements
    </div>
    <div class="mesh-section-xs--gap-4">
      This one too
    </div>
  </div>
</div>
```

## Push and pull

You can also pull and push units, so that you dont have to add garbage units
to align something accordingly. So now you dont have to do this:

```html
<div class="mesh-container">
  <div class="mesh-unit-xs--col-5">
  </div>
  <div class="mesh-unit-xs--col-7">
  </div>
</div>
```

But instead you can do this:

```html
<div class="mesh-container">
  <div class="mesh-unit-xs--col-7 mesh-unit--push-col-5">
  </div>
</div>
```
