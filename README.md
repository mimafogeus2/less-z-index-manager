# less-z-index-manager

## What
A simple Less tool to manage z-index number without meddling with numbers.

## Why
Because managing z-index is an unecessary management of numbers in its best case, and an annoying chaos in its worst case.

## Example
```
import ('path/to/less-z-index-manager.less')

// Generate your z-index list...:
.my-z-indices {
  @layers-list: lightbox, modal, top-bar, error;
  @spacing: 1000; // OPTIONAL. Default is 100;
  .get-z(@layers-list, @spacing);
}

// ... and use it like this:
.my-modal {
  ...
  z-index: .my-z-indices[modal];
}

// You get a number, so you can use it with arithmetics as well:
.my-modal {
  .child-slightly-above-modal {
    z-index: .my-z-indices[modal] + 1;
  }
}
```
