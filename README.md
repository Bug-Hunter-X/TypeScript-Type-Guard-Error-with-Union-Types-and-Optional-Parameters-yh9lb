# TypeScript Type Guard Bug

This repository demonstrates a common error in TypeScript related to type guards and union types, specifically when dealing with optional parameters or values that could be null or undefined.  The bug arises because TypeScript's type guards might not exhaustively check all possible values within a union type, leading to runtime errors even if the code compiles without errors.

## Bug Description
The `greet` function takes a string or null as input. It handles null correctly, but it fails when an undefined value is passed. This is because the type guard `name === null` only checks for null, not undefined.  TypeScript's type system doesn't catch this, resulting in a runtime error.

## Solution
The solution involves a more robust type guard that handles both null and undefined explicitly, or by using a different approach that avoids the need for such a guard.