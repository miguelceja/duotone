# Duotone Sass Mixins
Sass mixins to create a duotone effect on both inline and background images.

These mixins take advantage of the `mix-blend-mode` and `filter` CSS properties.  The mixins allow you to choose a main color, contrast value, and a mix-blend mode.

It includes a fallback for browsers that don't support the `filter` and 'mix-blend-mode` css properties.



HTML
```
<!-- BG Image -->
<div class="img-container duotone-bg-img-container--green">
  <div class="duotone-bg-img" style="background-image: url(https://images.unsplash.com/photo-1493849749377-e4f82d0a8319?auto=format&fit=crop&w=748&q=60&ixid=dW5zcGxhc2guY29tOzs7Ozs%3D);"></div>
</div>

<!-- Inline Image -->
<div class="img-container duotone-inline-img-container--darkblue">
  <img src="/images/my-inline-image.jpg" alt="">
</div>
```

CSS
```
.duotone-bg-img-container {
  &--darkred {
    @include duoToneBg(#d42747, 1.1, multiply);
  }

  &--darkblue {
    @include duoToneBg(#0063bb, 1.1, multiply);
  }

  &--green {
    @include duoToneBg(#2eb27a, 1.1, multiply);
  }
}

.duotone-inline-img-container {
  &--darkblue {
    @include duotoneInline(#0061b8, 1.1, multiply);
  }

  &--darkred {
    @include duotoneInline(#d42747, 1.1, multiply);
  }

  &--green {
    @include duotoneInline(#2eb27a, 1.1, multiply);
  }
}
```


