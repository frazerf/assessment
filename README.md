# Assessment

## HTML/CSS Knowledge

---

### A breif description of the Box Model

Every element in CSS is a box of some description - `<div>`, `<span>`, `<button>`, etc, and each box has four different parts to it. The inner most part is the content itself, followed by the padding which surrounds the content, next is the border which wraps around the padding and lastly is margin of that box.

We can give style properties to each one of these parts. So for instance if we had a `<div>` on our page with “Hello World” as it’s content, we could do something like this -

```
div {
	background: blue;
	padding: 20px;
	border: 5px solid red;
	margin: 20px;
}
```

If we were to view our box it would have our content “Hello World” with a blue background and padding around the content of 20px in every direction. Around that would be a red border with a width of 5px and lastly we would have a margin of 20px surrounding the border.

If we were to create another `<div>` and add it directly below our original one we would see the exact same box as they share the same css properties. However, the `<div>`’s wouldn’t have a 40px (20px x 2) margin separating them. With the box model, margin’s collapse and take on the largest margin. So if we changed the second `<div>` to have a margin of 50px, the margin between both boxes would be 50px as the top `<div>`’s 20px margin would collapse and make way for the 50px of the second `<div>`.

If you were to add an explicit height to the first `<div>` of 100px, it would give the content a height of 100px, followed by 20px x 2 for the top and bottom padding and 5px x 2 for the top and bottom border to give our element a total height of 150px (margin does not count towards the height).

Nowadays we use the “box-sizing: border-box” declaration on all elements so we can set the explicit width and height of our element from the border down to the content. This means we don’t have to do any math to account for padding and borders of an element.
