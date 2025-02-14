---
title: AutoComplete may not work
author: simonxjx
manager: willchen
audience: ITPro
ms.service: office-perpetual-itpro
ms.topic: article
ms.author: v-six
---

# AutoComplete may not work

## Symptoms

You type text in a cell in Microsoft Excel. The first few characters of the text that you type match an existing entry in that column. When this occurs, the AutoComplete feature may not automatically fill in the remaining characters.

## Cause

In Microsoft Excel, the AutoComplete feature may not fill in the remaining characters if the algorithm that Excel uses detects a header row in the list.

## More Information

### Example

When you use the steps in the following example, the AutoComplete feature does not appear to function properly.

1. Save and close any open workbooks, and then create a new workbook.
2. In cell A1, type ABC in uppercase.
3. In cell A2, type a in lowercase and do not press ENTER.

   The AutoComplete feature automatically inserts "aBC" in cell A2.

4. Continue typing abc in lowercase in cell A2, and then press ENTER.

   This overwrites the text that is suggested by AutoComplete.

5. In cell B1, type ABC in uppercase.
6. In cell B2, type a in lowercase and do not press ENTER.

   The AutoComplete feature does not automatically suggest "aBC" in cell B2 as it does in step 3.

Because the characters in cell A1 are all uppercase, and the characters in cell A2 are all lowercase, Microsoft Excel determines that row 1 is a list header row. The algorithm for the AutoComplete feature does not generate suggested text if the first row is considered a list header row. This behavior also occurs if characters in cell A2 are uppercase and lowercase.