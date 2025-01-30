# PHP Foreach Loop with References and Unset() - Unexpected Behavior

This repository demonstrates an uncommon bug in PHP related to the use of references within a foreach loop when calling unset() on array elements.  Modifying arrays directly within a foreach loop using references can lead to unexpected behavior and skipped iterations due to how PHP internally handles array indices.

The `bug.php` file contains the buggy code, while `bugSolution.php` presents a corrected version.

## Bug Description
When using references (`&`) in a foreach loop and calling `unset()` on array elements, the loop's internal pointer might skip elements due to the changing indices. This is particularly important when you're trying to remove certain elements within the loop.