### 1.1 Flexbox properties

- flex-direction, flex-wrap, justify-content, align-items, flex-grow, flex-shrink

  ```CSS
  .container {
    display: flex; /* or inline-flex */
  }
  ```

  - flex-direction
   
     - row (default): left to right in ltr; right to left in rtl
     - row-reverse: right to left in ltr; left to right in rtl
     - column: same as row but top to bottom
     - column-reverse: same as row-reverse but bottom to top

        ```css
        .container {
            flex-direction: row | row-reverse | column | column-reverse;
        }
        ```

  - flex-wrap

    - nowrap (default): all flex items will be on one line
    - wrap: flex items will wrap onto multiple lines, from top to bottom.
    - wrap-reverse: flex items will wrap onto multiple lines from bottom to top.
    
        ```css
        .container {
            flex-wrap: nowrap | wrap | wrap-reverse;
        }
        ```

  - justify-content

    - flex-start (default): items are packed toward the start of the flex-direction.
    - flex-end: items are packed toward the end of the flex-direction.
    - center: items are centered along the line
    - space-between: items are evenly distributed in the line; first item is on    the start line, last item on the end line
    - space-around: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
    - space-evenly: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

      ```css
        .container {
            justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
        }
      ```
  - align-items

    - stretch (default): stretch to fill the container (still respect min-width/max-width)
    - flex-start: items are placed at the start of the cross axis.
    - flex-end: items are placed at the end of the cross axis.
    - center: items are centered in the cross-axis.
    - baseline: items are aligned such as their baselines align

        ```css
        .container {
            align-items: stretch | flex-start | flex-end | center | baseline;
        }
        ```

### 1.2 Grid Layout

- grid-template-columns, grid-template-rows, grid-gap, grid-column, grid-row

  - grid-template-columns

    ```css
    .grid-container {
        display: grid;
        grid-template-columns: auto auto auto auto;
        grid-template-columns: 250px 250px 250px 250px;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-template-columns: repeat(4,25%);
        grid-template-columns: repeat(4,1fr);
        grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    }
    ```

  - grid-gap

    ```CSS 
    .grid-container {
        display: grid;
        <!-- grid-gap: grid-row-gap grid-column-gap; -->
        grid-gap: 20px 20px;
        <!-- grid-row-gap: length; -->
        grid-row-gap: 20px;
        grid-column-gap: 20px;
    }
    ```

  - grid-column

    ```css
    .grid-container {
        display: grid;
    }
    .grid-item {
        grid-column: 1 / 3;
        grid-column: 1 / span 3;
        grid-column-start: 1;
        grid-column-end: 3;
    }
    ```

  - grid-template-areas

    ```css
    .item1 { grid-area: header; }
    .item2 { grid-area: menu; }
    .item3 { grid-area: main; }
    .item4 { grid-area: right; }
    .item5 { grid-area: footer; }

    .grid-container {
    grid-template-areas:
        'header header header header header header'
        'menu main main main right right'
        'menu footer footer footer footer footer';
    }
    ```