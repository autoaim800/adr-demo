# [ADR-001] Use 'val' for MutableStateFlow Backing Fields

## Status
Accepted

## Context
In our codebase analysis, we identified inconsistent usage of `var` vs `val` for `MutableStateFlow` backing fields:

```kotlin
// Current inconsistent patterns:
private var _state1 = MutableStateFlow<State>(State.Loading)  // ❌ Using 'var'
private val _state2 = MutableStateFlow<State>(State.Loading)  // ✅ Using 'val'
```
