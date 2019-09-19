# Grid

## Grid values

| Breakpoints   | Viewport family | Columns | Margins | Gutters |
| ------------- | --------------- | ------- | ------- | ------- |
| 320 — 599     | Small           | 4       | 16px    | 16px    |
| 600 — 1135    | Medium          | 8       | 36px    | 36px    |
| 1136 — ∞      | Large           | 12      | 64px    | 36px    |

*Margins are for left/right edges, while gutters are margins between columns in a row.*

## Design considerations

* To support Internet Explorer, `Grid` will use `flex` layout under the hood
* Grid values will live in the `Theme`, and the component will pick them up from there

## API

### Row

* `gutter` - optionally, it can override the margin between columns for a specific `Row`
* `align` - vertical alignment of columns inside a row (`top`, `middle` or `bottom`)
* `justify` - horizontal alignment of columns inside a row (`start`, `end` ...)

### Col

* `offset` - the number of columns to offset, starting from the left
* `span` - the number of columns to occupy

```js
import { Row, Col } from 'baseui/grid';

export default () => (
  <div>
    <Row>
      <Col span={6}>col-6</Col>
      <Col span={6}>col-6</Col>
    </Row>
    <Row>
      <Col span={4}>col-4</Col>
      <Col span={4}>col-4</Col>
      <Col span={4}>col-4</Col>
    </Row>
  </div>
)

```