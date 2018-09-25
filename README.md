# Plant Type
My current typography system. Sizes translate from Sketch app, convert to easy to read REMs as 25px = 2.5rem.

## Usage example 

### default usage
```scss
p {
  @include typography(p,p);
}
p.leadin {
  @include typography(leadin,leadin);
}
```

### inherit line height needed
``` scss
p {
  @include typography(info,n);
}
```

(i): the first p references the declared $font-sizes, and the second p references the declared $line-heighs
