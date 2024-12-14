# MongoDB Aggregation Pipeline Error: Incorrect use of $inc operator

This repository demonstrates an error in using the `$inc` operator within a MongoDB aggregation pipeline.  The `$inc` operator is designed to increment numeric fields in documents, but it's incorrectly applied here, leading to unexpected results. The solution shows the correct approach using `$add` operator.

## Bug Description
The original code attempts to increment the 'count' field after grouping using `$group`. This is incorrect, as `$inc` is used within update operators, not in aggregation pipelines. This attempt will either throw an error or produce incorrect results.

## Solution
The solution shows how to correctly add 1 to the `count` field, using the `$add` operator within the `$project` stage.