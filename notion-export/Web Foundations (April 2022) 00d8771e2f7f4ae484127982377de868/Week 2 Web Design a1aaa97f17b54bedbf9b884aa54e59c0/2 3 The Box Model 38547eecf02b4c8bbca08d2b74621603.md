# 2.3 The Box Model

*Estimated Time: 30 minutes*

---

> Everything in CSS has a box around it.
****
> 
> 
> *[MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)*
> 

CSS thinks in rectangles.

Everything on the screen — even if it shows up as a circle, triangle, or squiggle — has a dedicated rectangle of space when browser figures out where to put it on the screen.

This is an illustration of the **Box Model**. Each element has margin, border, padding, and content.

If you know the Box Model, you can use CSS to control how much space the browser puts between the rectangles. It’s a key set of tools for you to use in making a page look good.

From the inside, going outwards:

- **Content** is what’s inside an element.
- **Padding** is the space between the element and the border.
- **Border** is a line around the element that can have some width.
- **Margin** is the space between elements.

These properties apply to the top, right, bottom, and left of the element.

![The CSS Box Model. Nested rectangles labeled Margin, Border, Padding, and Content](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/box-model.png)

The CSS Box Model. Nested rectangles labeled Margin, Border, Padding, and Content

## Box Model in the DevTools

<aside>
📽️ **Video**: Viewing the Box Model in the DevTools 

Before you dive deeper into the box model, here’s a quick tutorial on how to view the box model in the DevTools.

[https://www.loom.com/share/76f1b79a6bad45f18f6944278776bd08](https://www.loom.com/share/76f1b79a6bad45f18f6944278776bd08)

</aside>

# The Box Model

<aside>
🎥 **Video:** Learn the CSS Box Model
This video from Web Dev Simplified explores the different parts of the Box Model covered in this lesson.

[https://www.youtube.com/watch?v=rIO5326FgPE](https://www.youtube.com/watch?v=rIO5326FgPE)

</aside>

## Content

Content is what’s inside the element.

It doesn’t have a single CSS property that sets how big it is. Instead, it’s the sum of the sizes of all the stuff inside.

For some elements, you can set the `width` and `height` properties to control the dimensions, but this doesn’t always work.

![content-box.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/content-box.png)

## Padding

Padding is the space between an element and its border.

It’s controlled by the `padding` properties:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

You can set any of the properties on their own, or set them all at once with `padding`.

Check out the [MDN docs on padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) for an interactive example and more information.

![padding-box.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/padding-box.png)

### **`padding` example**

The `padding` shorthand sets the top, right, bottom, and left in one line.

```css
/* top | right | bottom | left */
padding: 30px 12px 30px 12px;
```

![11C0BCA8-A34F-4DC4-BD90-ACD739E1AC06-2762-000087D271E01487.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/11C0BCA8-A34F-4DC4-BD90-ACD739E1AC06-2762-000087D271E01487.png)

- **Further Exploration**: CSS direction shorthands
    
    These are all equivalent:
    
    ```css
    /* top | right | bottom | left */
    padding: 30px 12px 30px 12px;
    
    /* top | right and left | bottom  */
    padding: 30px 12px 30px;
    
    /* top and bottom | right and left  */
    padding: 30px 12px;
    ```
    
    If you leave out some of the 4 values, they get ‘filled in’ by the earlier value along the same axis.
    
    If you use just 1 value, it applies to all 4 sides, so `padding: 1px` is the same as `padding: 1px 1px 1px 1px`.
    
    The same shorthand works for the `border` and `margin` properties too.
    

## Border

Border is a line around an element, with a width, color, and style. It’s controlled by a set of `border` properties.

- `border-width`
- `border-color`
- `border-style`

These can each be set for the whole element, or for the top, right, bottom, or left, like `border-top-color` or `border-bottom-style`.

![border-box-model.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/border-box-model.png)

### **`border` example**

The `border` shorthand sets the width, style, and color for all 4 sides.

```css
/* width | style | color */
border: 4px dashed green;
```

![F571BD73-CE94-4BEA-989B-B07E1BBFA094-2762-000087732A9B2CA7.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/F571BD73-CE94-4BEA-989B-B07E1BBFA094-2762-000087732A9B2CA7.png)

See the [MDN docs on border](https://developer.mozilla.org/en-US/docs/Web/CSS/border) for more information.

## Margin

Margin is the space between one element’s border and another element. It’s controlled by a set of `margin` properties.

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

Like the other box model properties, `margin` is a shorthand for setting all of the properties at once.

![margin-box.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/margin-box.png)

### `margin` e**xample**

`margin` is shown in yellow. It’s applied to the blue element.

```css
margin: 20px;
```

20 pixels of margin on all sides.

![81AB221B-99EF-4482-BB12-FD5C2F73ED40-2762-000088712844B9FB.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/81AB221B-99EF-4482-BB12-FD5C2F73ED40-2762-000088712844B9FB.png)

```css
margin: 20px 0;
```

20 pixels of top and bottom margin, 0 left and right margin.

![05992734-2715-4985-AFCD-A0CFE7F277DF-2762-0000886DE89F5B32.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/05992734-2715-4985-AFCD-A0CFE7F277DF-2762-0000886DE89F5B32.png)

```css
margin: 0;
```

0 margin on the top, bottom, left, and right.

![CBFF83DD-EDE8-47FA-9ED2-0F6F61D702F1-2762-0000886C154F42D2.png](2%203%20The%20Box%20Model%2038547eecf02b4c8bbca08d2b74621603/CBFF83DD-EDE8-47FA-9ED2-0F6F61D702F1-2762-0000886C154F42D2.png)

## Practice: Box Model

<aside>
↔️ Practice applying the box model properties. Follow the instructions in the Repl.

Access the repl here: [https://replit.com/team/tk5-web/23-Practice-Box-Model](https://replit.com/team/tk5-web/23-Practice-Box-Model) or below

</aside>

[https://replit.com/team/tk5-web/23-Practice-Box-Model](https://replit.com/team/tk5-web/23-Practice-Box-Model)

- **Further Reading**: The Box Model
    - MDN’s [page on the box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model) explains the components of the box model in more detail.
    - [Shay Howe’s tutorial on HTML and CSS](https://learn.shayhowe.com/html-css/opening-the-box-model/) is another useful explanation of how the Box Model works.
    - [Colt Steele’s video on the Box Model](https://www.youtube.com/watch?v=M1xEi_BBW1I) is great if you enjoy video content
    
    They explain some of the topics we’ve skipped over here, like
    
    - box-sizing
    - margin collapse
    - `display: inline-block`
    - ‘inner’ and ‘outer’ display

## The `**margin: auto` trick**

Setting `margin: auto` is a one way to center an element horizontally. It sets the left and right margins to whatever is needed to center the element. It doesn’t work for vertical alignment.

## Block and inline boxes

So, one thing that can be pretty confusing. All this box model stuff is true for most elements, but... some elements don’t actually work that way!

Elements like `<a>`, `<span>`, `<strong>`, and `<em>` are **inline elements**. They don’t go onto a whole new line like a `<p>` or a `<div>`. Inline elements get a slightly different version of the box model than **block** elements.

Here are the differences for **inline boxes** (from [MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)):

- The box will not break onto a new line.
- The `width` and `height` properties will not apply.
- Vertical padding, margins, and borders will apply but *will not cause other inline boxes to move away from the box*.

Horizontal padding, margins, and borders will apply and will cause other inline boxes to move away from the box.

- **Further Exploration**: Block and Inline
    
    MDN’s [page on the Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model) explains more about block and inline boxes.
    
    In the next lesson, you’ll also learn about the `display` property, which can control which kind of box an element has.
    

## Practice: Block and Inline

<aside>
🟦 Practice using the `display` property and your new understanding of inline and block elements.

Access the repl here: [https://replit.com/team/tk5-web/24-Practice-Block-and-Inline](https://replit.com/team/tk5-web/24-Practice-Block-and-Inline) or below

</aside>

[https://replit.com/team/tk5-web/24-Practice-Block-and-Inline](https://replit.com/team/tk5-web/24-Practice-Block-and-Inline)

## CSS Units

So far, we’ve used pixels (`px`) as the units in our examples. CSS has lots of different kinds of units that are useful in different situations.

Pixels are not the only units! CSS actually has more than 10 units you can use. For now, the only one we’ll mention is `em`. `1em` is the same as saying “the current font size”. So, to make text three quarters the size of the surrounding text, you could use `font-size: 0.75em`.

You can also specify values in terms of percentages. An element with `width: 50%` will try to take up 50% of the width of its parent element.

- **Further Exploration**: CSS Units
    
    The [MDN page on CSS values and units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units) goes into depth about the different units available for different values.
    

---

<aside>
<img src="../Lesson%200%20Learning%20With%20Kibo%206427d2f5f1ae4576a3b083dd8476d915/man-in-hike.png" alt="../Lesson%200%20Learning%20With%20Kibo%206427d2f5f1ae4576a3b083dd8476d915/man-in-hike.png" width="40px" /> Next up: [Layout and Positioning](2%204%20Layout%20466ffa1962ca4a3cba06e17c156e6424.md)

</aside>