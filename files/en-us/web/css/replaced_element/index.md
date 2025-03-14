---
title: Replaced elements
slug: Web/CSS/Replaced_element
page-type: guide
---

{{CSSRef}}

In [CSS](/en-US/docs/Web/CSS), a **replaced element** is an element whose representation is outside the scope of CSS; they're external objects whose representation is independent of the CSS formatting model.

Put in simpler terms, they're elements whose contents are not affected by the current document's styles. The position of the replaced element can be affected using CSS, but not the contents of the replaced element itself. Some replaced elements, such as {{HTMLElement("iframe")}} elements, may have stylesheets of their own, but they don't inherit the styles of the parent document.

The only other impact CSS can have on a replaced element is that there are properties which support controlling the positioning of the element's content within its box. See [Controlling object position within the content box](#controlling_object_position_within_the_content_box) for further information.

## Replaced elements

Typical replaced elements are:

- {{HTMLElement("img")}}
- {{HTMLElement("video")}}
- {{HTMLElement("iframe")}}
- {{HTMLElement("embed")}}
- {{HTMLElement("fencedframe")}}

Some elements are treated as replaced elements only in specific cases:

- {{HTMLElement("option")}}
- {{HTMLElement("audio")}}
- {{HTMLElement("canvas")}}
- {{HTMLElement("object")}}

HTML spec also says that an {{HTMLElement("input")}} element can be replaced, because {{HTMLElement("input")}} elements of the `"image"` type are replaced elements similar to {{HTMLElement("img")}}. However, other form controls, including other types of {{HTMLElement("input")}} elements, are explicitly listed as non-replaced elements (the spec describes their default platform-specific rendering with the term "Widgets").

Objects inserted using the CSS {{cssxref("content")}} property are _anonymous replaced elements_. They are "anonymous" because they don't exist in the HTML markup.

## Using CSS with replaced elements

CSS handles replaced elements specifically in some cases, like when calculating margins and some `auto` values.

Note that some replaced elements, but not all, have intrinsic dimensions or a defined baseline, which is used by some CSS properties, such as {{cssxref("vertical-align")}}. Only replaced elements can ever have intrinsic dimensions.

### Controlling object position within the content box

Certain CSS properties can be used to specify how the object contained within the replaced element should be positioned within the element's box area. These are defined by the [CSS Images](https://drafts.csswg.org/css-images/) specification:

- {{cssxref("object-fit")}}
  - : Specifies how the replaced element's content object should be fitted to the containing element's box. The `object-fit` property has no effect on {{HTMLElement("iframe")}}, {{HTMLElement("embed")}}, and {{HTMLElement("fencedframe")}} elements.
- {{cssxref("object-position")}}
  - : Specifies the alignment of the replaced element's content object within the element's box.

## See also

- [HTML Spec](https://html.spec.whatwg.org/multipage/rendering.html#replaced-elements)
- {{glossary("void element", "Void elements")}}
- CSS key concepts:
  - [CSS syntax](/en-US/docs/Web/CSS/CSS_syntax/Syntax)
  - [At-rules](/en-US/docs/Web/CSS/CSS_syntax/At-rule)
  - [Comments](/en-US/docs/Web/CSS/CSS_syntax/Comments)
  - [Specificity](/en-US/docs/Web/CSS/CSS_cascade/Specificity)
  - [Inheritance](/en-US/docs/Web/CSS/CSS_cascade/Inheritance)
  - [Box model](/en-US/docs/Web/CSS/CSS_box_model/Introduction_to_the_CSS_box_model)
  - [Layout modes](/en-US/docs/Web/CSS/Layout_mode)
  - [Visual formatting model](/en-US/docs/Web/CSS/Visual_formatting_model)
  - [Margin collapsing](/en-US/docs/Web/CSS/CSS_box_model/Mastering_margin_collapsing)
  - Values
    - [Initial values](/en-US/docs/Web/CSS/CSS_cascade/initial_value)
    - [Computed values](/en-US/docs/Web/CSS/CSS_cascade/computed_value)
    - [Used values](/en-US/docs/Web/CSS/CSS_cascade/used_value)
    - [Actual values](/en-US/docs/Web/CSS/CSS_cascade/actual_value)
  - [Value definition syntax](/en-US/docs/Web/CSS/CSS_Values_and_Units/Value_definition_syntax)
  - [Shorthand properties](/en-US/docs/Web/CSS/CSS_cascade/Shorthand_properties)
