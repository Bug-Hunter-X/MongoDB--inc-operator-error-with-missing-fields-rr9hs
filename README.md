# MongoDB $inc Operator Error with Missing Fields

This repository demonstrates an uncommon error that can occur when using the `$inc` operator in MongoDB. The `$inc` operator is used to increment or decrement a numeric field in a document. However, if the field does not exist in the document, the operation may fail silently or produce unexpected results.

## Bug Description

The provided `bug.js` file contains an example of how this issue can manifest. When the `$inc` operator is used with a field that does not exist, the update operation may not result in the desired effect. This can be problematic if relying on the correct increment value for other operations.

## Bug Solution

The solution file, `bugSolution.js`, shows how to address this issue by using the `$setOnInsert` operator along with `$inc`. This ensures the field is created with a default value if it doesn't exist, then correctly increments the value if it does.