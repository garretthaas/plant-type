# Plant Type
My current typography boilerplate. Intentionally bare with room to grow.

## Sizes translate from Sketch app by default
- Convert to easy-to-read REMs
- 25px = 2.5rem

## Usage example 

### default usage
```scss
$font-sizes: ( // from sketch app font "Size" property
    'p'       : ( 21 ),
    'leadin'  : ( 35 ),
    'info'    : ( 16 ),
);
$line-heights: ( // from sketch app "Line" spacing property
    'p'       : ( 21 ),
    'leadin'  : ( 35 ),
    'info'    : ( q  ),
);
```
( i ): declared variables get called as mixin args in your scss.

```scss
p {
  @include typography(p,p);
}
p.leadin {
  @include typography(leadin,leadin);
}
```
( i ): the first argument references a `$font-size` variable and the second argument references a `$line-height` variable reclared in the mixin.

( i ): these can be anything you assign in the mixin variables...I created matching variable names becuase that makes sense to me `@include typography(foo,bar);`, `@include typography(foo,foo);`, `@include typography(bar,bar);`

### inherit line height needed
``` scss
p {
  @include typography(info,n);
}
```

( i ): If `line-height:inherit;`

## Extend
Font Families are separated from the `@typography(arg,arg);` mixin.
Need more or less font-size and line-height variables? Just declare more or remove some.
