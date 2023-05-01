# vue-retro-grid
NPM package: a fully-customizable, moving 3D grid, in the 80s retro / synthwave / vaporwave style.
Compatible with Vue.js.

## PREVIEW

<div align="center">
	<img src="https://github.com/IlanAzoulay/vue-retro-grid/tree/master/preview/retro_preview.gif" alt="Preview GIF">
</div>

Live example on [my website](https://ilan-azoulay.com/)

## FEATURES

The grid will be placed in absolute position, ideal for covering the background of your page.
You can decide all the colors, how high/low the grid goes, its animation speed, the amount of lines, and much more!

## INSTALLATION

```bash
npm i vue-retro-grid
```

## HOW TO USE

### BASICS

Add this to the *<script>* part of your Vue file

```js
import VueRetroGrid from 'vue-retro-grid';

export default {
  components: {
    VueRetroGrid
  }
}
```

And this in the HTML part:

```html
    <vue-retro-grid/>
```

We will discuss the input props for customization just below. All of them are optional.

### CUSTOMIZE WITH INPUT PROPERTIES / PROPS

Here is the full list of props you can customize:

#### --- Animation props

##### 1. updateInterval

Type: `Number`\
Unit: `Milliseconds`\
Default: `20`\
Refresh rate of the animation

##### 2. framesPerLoop

Type: `Number`\
Unit: `Milliseconds`\
Default: `8`\
Loop animation every *framesPerLoop* refreshes of the animation

#### --- Geometry props - Horizontal lines

##### 3. startHeight

Type: `Number`\
Unit: `%`\
Default: `50`\
Y coordinate of the perspective endpoint of the grid

##### 4. amountHorizontals

Type: `Number`\
Default: `15`\
Amount of horizontal lines making up the grid (looped)

##### 5. horizontalFactorInput

Type: `Number`\
Default: `1.6`\
Increase factor in gaps between horizontal lines. Changing this prop changes the perceived perspective of the fake 3D effect.
**Warning: cannot be below 1**

#### --- Geometry props - Vertical lines

##### 6. amountVerticals

Type: `Number`\
Default: `6`\
Amount of vertical lines

##### 7. verticalAngleFactorInput

Type: `Number`\
Default: `1.6`\
Increase factor in Angle gaps between vertical lines. Changing this prop changes the perceived perspective of the fake 3D effect.
**Warning: cannot be below 1**

##### 8. offsetVerticalLinesY

Type: `Number`\
Unit: `%`\
Default: `0.4`\
Making vertical lines slightly lower or higher than startHeight to fit better visually. If your vertical lines do not connectly perfectly with the higher horizontal line, you can increase or decrease this prop to adjust their Y coordinate.

##### 9. offsetVerticalLinesX

Type: `Number`\
Unit: `%`\
Default: `0`\
Offset to make the vertical lines go more to the right or left, for some reason.

#### --- Stylistic props

##### 10. blurredPerspective

Type: `Boolean`\
Default: `false`\
Adding a depth of field blur effect. Can improve the visuals greatly to switch on this prop.

##### 11. gridColor

Type: `String`\
Default: `'blueviolet'`\
Color of the grid lines

##### 12. backgroundColor

Type: `String`\
Default: `'#24162F'`\
Color of the background screen (and foreground blur if turned on)

### Example

Overall, if you want to specify all props, this would be the result when calling the component:

```html
<vue-retro-grid 
    :update-interval="20"
    :frames-per-loop="8"
    :start-height="50"
    :amount-horizontals="15"
    :horizontal-factor-input="1.6"
    :amount-verticals="6"
    :vertical-angle-factor-input="1.6"
    :offset-vertical-lines-y="0.4"
    :offset-vertical-lines-x="1"
    :blurred-perspective="true"
    :grid-color="'blueviolet'"
    :background-color="'#24162F'"
	/>
```

## LICENSE

Copyright 2023 Ilan Azoulay

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), 
to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, 
and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, 
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
