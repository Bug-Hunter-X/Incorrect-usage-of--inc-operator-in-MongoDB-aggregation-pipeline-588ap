# Incorrect usage of $inc operator in MongoDB aggregation pipeline
This example demonstrates an incorrect usage of the `$inc` operator within a MongoDB aggregation pipeline's `$project` stage.  The `$inc` operator is designed for updating documents, not for creating new calculated fields within the aggregation pipeline. This can lead to unexpected results or errors.

## Bug
The provided code attempts to increment the `count` field using `$inc` within the `$project` stage.  This will not work as intended, resulting in either an error or unexpected values.

## Solution
The correct approach uses the `$add` operator to achieve the desired increment.  `$add` correctly calculates the incremented value and adds it to the projected document.
