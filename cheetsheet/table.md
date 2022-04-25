### :bookmark: Table

As we all know, one table is composed of columns and rows, and each column might have one specific column name. Usually, the first row is called as **the Header** and each cell in the header saves one column name.

The syntax of creating a table is quiet easy (_**It doesn't matter if the first**_ ```|``` _**and the last**_ ```|``` _**on each line are omitted**_).

```
| Column 1 | Column 2 |
| -------- | -------- |
|  Cell 1  |  Cell 2  |
```

or

```
Column 1 | Column 2
-------- | --------
 Cell 1  |  Cell 2 
```

We use any number of ```---``` to separate the header row and other rows. Between columns of each row, we only need to use just one ```|``` so that we can tell apart different columns.

&nbsp;:heavy_exclamation_mark: &nbsp;&nbsp;**We must reserve at least one blank line before we create tables, otherwise it won't work at all.**
:x: **Unfortunately, we can't create some comple table operations, like merging some cells or change colors in Markdown, while we can use HTML to implement these.**

---

#### :bulb: Practice: A Simple Table

In this part, we use the above syntax to create a simple table of personal information.

| Name | Gender | Age |
| ---- | ------ | --- |
| Leo  | Male   | 22  |
| Lucy | Female | 12  |

---

#### :bulb: Alignment

From this simple info table, we can see that the header row is bolder that other rows, and all cells are aligned to **the left** automatically. Except for left alignment, we can align the cell to **the right** and **the center** as well. All syntax details are as follows (**_all changes are happen on the separate dash line between the header and the others_**):

|              | Left alignment | Center alignment | Right alignment |
|     ---      |     :---       |      :---:       |      ---:       |
| **Example**  |     Left       |      Center      |      Right      |
| **Syntax**   |  ```:---```    |   ```:---:```    |    ```---:```   |
