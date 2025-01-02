# Dart Null-Aware Operator and Getter/Setter Unexpected Behavior

This repository demonstrates a subtle bug related to the null-aware operator (?.) in Dart when used with getter/setter methods that handle null values.

## Bug Description

The `bug.dart` file showcases a scenario where a class member can be null.  A getter is implemented to return 0 if the member is null and a setter to update the value.  The null-aware operator is not needed in this case because the getter itself prevents a null pointer exception.  However, other developers might try using `?.` which does not change the output but could obscure the issue and potentially make the code harder to maintain or debug.