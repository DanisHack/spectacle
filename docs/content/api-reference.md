---
title: API Reference
order: 5
---

<a name="api-reference"></a>

# API Reference

In Spectacle, presentations are composed of a set of base tags. We can separate these into three categories: [Main tags](#main-tags), [Semantic tags](#semantic-tags) & [Style tags](#style-tags).

<a name="main-tags"></a>

## Main Tags

These are the bare bones of a Spectacle presentation, the two most essential tags you'll need to assemble a slideshow.

<a name="deck"></a>

### Deck

Wraps the entire presentation and carries most of the overarching slide logic, like theme and template context.

| Props            | Type                                                                       |
| ---------------- | -------------------------------------------------------------------------- |
| theme            | [Styled-system theme object](/docs/themes)                                 |
| template         | [Template render function](#deck-template)                                 |
| transitionEffect | "fade", "slide", "none", or [custom transition object](#transition-object) |

<a name="slide"></a>

### Slide

Wraps a single slide within your presentation; identifies what is contained to a single view. If a transition effect is applied to this slide, it will override the Deck-specified transition.

| Props              | Type                                                                       |
| ------------------ | -------------------------------------------------------------------------- |
| backgroundColor    | PropTypes.string                                                           |
| backgroundImage    | PropTypes.string                                                           |
| backgroundOpacity  | PropTypes.number                                                           |
| backgroundPosition | PropTypes.string                                                           |
| backgroundRepeat   | PropTypes.string                                                           |
| backgroundSize     | PropTypes.string                                                           |
| scaleRatio         | PropTypes.number                                                           |
| slideNum           | PropTypes.number                                                           |
| template           | PropTypes.func                                                             |
| textColor          | PropTypes.string                                                           |
| transitionEffect   | "fade", "slide", "none", or [custom transition object](#transition-object) |

<a name="typography-tags"></a>

## Typography Tags

These tags are for displaying textual content.

| Tag Name                                       | Theme Props                                                                                                             | Additional Props           | Default Props                                                                                                                                                    |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a name="text"></a>**Text**                    | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)       | —                          | **color**: primary<br /> **fontFamily**: text<br />**fontSize**: text<br />**textAlign**: left<br />**margin**: textMargin                                       |
| <a name="heading"></a>**Heading**              | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)       | —                          | **color**: secondary<br /> **fontFamily**: header<br />**fontSize**: h1<br />**fontWeight**: bold<br />**textAlign**: center<br />**margin**: headerMargin       |
| <a name="link"></a>**Link**                    | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)<br /> | **href**: PropTypes.string | **color**: quaternary<br /> **fontFamily**: text<br />**fontSize**: text<br />**textDecoration**: underline<br />**textAlign**: left<br />**margin**: textMargin |
| <a name="quote"></a>**Quote**                  | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)<br /> | —                          | **color**: primary<br /> **fontFamily**: text<br />**fontSize**: text<br />**textAlign**: left<br />**borderLeft**: 1px solid secondary                          |
| <a name="ordered-list"></a>**OrderedList**     | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)       | —                          | **color**: primary<br /> **fontFamily**: text<br />**fontSize**: text<br />**textAlign**: left<br />**margin**: listMargin                                       |
| <a name="unordered-list"></a>**UnorderedList** | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)       | —                          | **color**: primary<br /> **fontFamily**: text<br />**fontSize**: text<br />**textAlign**: left<br />**margin**: listMargin                                       |
| <a name="list-item"></a>**ListItem**           | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)       | —                          | **margin**: listMargin                                                                                                                                           |
| <a name="code-span"></a>**CodeSpan**           | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br /> [**Typography**](/docs/props#typography)       | —                          | **fontFamily**: monospace<br />**fontSize**: text                                                                                                                |

<a name="layout-tags"></a>

## Layout Tags

These tags are for adding structure to your slides.

| Tag Name                           | Theme Props                                                                                                                                                                                                                       | Additional Props | Default Props     |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ----------------- |
| <a name="box"></a>**Box**          | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Position**](/docs/props#position)<br /> [**Border**](/docs/props#border)                                         | —                | —                 |
| <a name="flex-box"></a>**FlexBox** | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Position**](/docs/props#position)<br /> [**Border**](/docs/props#border)<br />[**Flex**](/docs/props#flex)<br /> | —                | —                 |
| <a name="grid"></a>**Grid**        | [**Layout**](/docs/props#layout)<br />[**Position**](/docs/props#position)<br />[**Grid**](/docs/props#grid)<br />                                                                                                                | —                | **display**: grid |

<a name="table-tags"></a>

## Table Tags

These tags are for adding tables with content to your slides.

| Tag Name                                   | Theme Props                                                                                                                                                                                   | Additional Props | Default Props                                                                                                                                       |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a name="table"></a>**Table**              | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Typography**](/docs/props#typography)<br /> [**Border**](/docs/props#border) | -                | **color**: primary<br />**fontFamily**: text<br />**fontSize**: text<br />**textAlign:** left<br />**margin**: listMargin                           |
| <a name="table-header"></a>**TableHeader** | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Typography**](/docs/props#typography)<br /> [**Border**](/docs/props#border) | -                | **color**: primary<br />**fontFamily**: text<br />**fontSize**: text<br />**fontWeight**: bold<br />**textAlign:** left<br />**margin**: listMargin |
| <a name="table-body"></a>**TableBody**     | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Typography**](/docs/props#typography)<br /> [**Border**](/docs/props#border) | -                | **color**: primary<br />**fontFamily**: text<br />**fontSize**: text<br />**textAlign:** left<br />**margin**: listMargin                           |
| <a name="table-row"></a>**TableRow**       | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Typography**](/docs/props#typography)<br /> [**Border**](/docs/props#border) | -                | **color**: primary<br />**fontFamily**: text<br />**fontSize**: text<br />**textAlign:** left<br />**margin**: listMargin                           |
| <a name="table-cell"></a>**TableCell**     | [**Space**](/docs/props#space)<br />[**Color**](/docs/props#color)<br />[**Layout**](/docs/props#layout)<br />[**Typography**](/docs/props#typography)<br /> [**Border**](/docs/props#border) | -                | **color**: primary<br />**fontFamily**: text<br />**fontSize**: text<br />**textAlign:** left<br />**margin**: listMargin                           |

<a name="appear"></a>

## Appear

Appear is a component that makes a component animate on the slide on key press. The default animation is opacity. It is currently required to specify the order of elements to be animated starting with `1`. Sequential `<Appear />` tags do not have to be in order.

| Props            | Type                          | Example                                        |
| ---------------- | ----------------------------- | ---------------------------------------------- |
| children         | PropTypes.string              | `<Text>Hi</Text>`                              |
| elementNum       | PropTypes.number              | `1`                                            |
| transitionEffect | { to: object; from: object; } | `{ to: { opacity: 1 }, from: { opacity: 0 } }` |

<a name="code-pane"></a>

## Code Pane

CodePane is a component for showing a syntax-highlighted block of source code. It will scroll for overflow amounts of code. The Code Pane will trim whitespace and normalize indents. It will also wrap long lines of code and preserve the indent. Optionally you can have the Code Pane fill the available empty space on your slide via the `autoFillHeight` prop. Themes are configurable objects and can be imported from the [prism-react-renderer themes](https://github.com/FormidableLabs/prism-react-renderer/tree/master/src/themes).

Additionally, `highlightStart` and `highlightEnd` props can be used to highlight certain ranges of code. Combine this with the [Stepper](#stepper) component to iterate over lines of code as you present.

| Props          | Type              | Example               |
| -------------- | ----------------- | --------------------- |
| autoFillHeight | PropTypes.boolean | `false`               |
| children       | PropTypes.string  | `let name = "Carlos"` |
| fontSize       | PropTypes.number  | `16`                  |
| highlightEnd   | PropTypes.number  | `2`                   |
| highlightStart | PropTypes.number  | `1`                   |
| language       | PropTypes.string  | `javascript`          |
| theme          | Prism Theme       | —                     |

```jsx
import lightTheme from 'prism-react-renderer/themes/nightOwlLight';

() => (
  <Slide>
    <CodePane language="javascript" theme={lightTheme}>
      {`
  function helloWorld() {
    console.log('Hello World!');
  }
`}
    </CodePane>
  </Slide>
);
```

<a name="stepper"></a>

## Stepper

Stepper is a render-prop component that allows you to step over a set of values in your presentation, providing the current value and step as arguments in the child function. Like [Appear](#appear), this iteration happens on key press. Especially useful for stepping through the [Code Pane](#code-pane) component.

```jsx
<Stepper values={[1, 2, 3]}>
  {(value, step) => <p>Current value: {value}</p>}
</Stepper>
```

<a name="full-screen"></a>

## FullScreen

FullScreen is a button that takes the presentation in and out of the browser's full screen mode. It can have a different color and be re-sized.

| Props | Type             | Example   |
| ----- | ---------------- | --------- |
| size  | PropTypes.number | `23`      |
| color | PropTypes.string | `#abc123` |

<a name="image"></a>

## Image

Image is a component to display a picture within a slide. It is analgous to an `<img>` tag and conforms to Layout and Position props.

| Props                                | Type             |
| ------------------------------------ | ---------------- |
| src                                  | PropTypes.string |
| [**Layout**](/docs/props#layout)     |                  |
| [**Position**](/docs/props#position) |                  |

<a name="markdown"></a>

## Markdown

Markdown is a component to author slides or slide content using Markdown. Regular Markdown tags get converted into Spectacle components. The `---` three dash marker is used to divide content into separate slides. When using the `---` as a slide delimiter it is required to set the `containsSlides` prop to `true`. Markdown also supports presenter notes using the `Notes:` marker.

| Props          | Type              | Example      |
| -------------- | ----------------- | ------------ |
| children       | PropTypes.string  | `# Hi there` |
| containsSlides | PropTypes.boolean | `true`       |

```jsx
<Slide>
  <Markdown>
    # Urql
    A highly customizable and versatile GraphQL client
  <Markdown>
  <Text>Made by Formidable</Text>
</Slide>
<Markdown containsSlides>
  # Writing queries

  When this hook is executed it will send the query and variables to your GraphQL API.

  ---

  # Writing mutations

  urql will by default come with a simple "document" cache. Each query with variables that is requested from a GraphQL API, the result will be cached completely.

  Notes: The easiest way to always display up-to-date data is to set the requestPolicy to 'cache-and-network'.
<Markdown>
```

<a name="notes"></a>

## Notes

Notes is a component that only renders in Presenter mode as presenter notes. It is used as the last component inside your slide but does not show on the deck.

| Props    | Type             | Example           |
| -------- | ---------------- | ----------------- |
| children | PropTypes.string | `Presenter Notes` |

```jsx
<Slide>
  <Heading>Urql</Heading>
  <Text>A highly customizable and versatile GraphQL client</Text>
  <Notes>
    Urql is a GraphQL client that exposes a set of React components and hooks.
  </Notes>
</Slide>
```

<a name="progress"></a>

## Progress

Progress is a component with no children that just shows dots for each slide in your deck. Visited and current slides are represented by a filled circle and future slides with just a stroke. The size and color are customizable.

| Props | Type             | Example   |
| ----- | ---------------- | --------- |
| size  | PropTypes.number | `23`      |
| color | PropTypes.string | `#abc123` |
