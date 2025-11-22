# ADR-001: Use 'val' for MutableStateFlow Backing Fields

## Decision
Use `val` for backing fields

## Context
**Forbidden:**
```kotlin
private var _state1 = MutableStateFlow<State>(State.Loading)  // ❌ Using 'var'
```

**Approved:**
```kotlin
private val _state2 = MutableStateFlow<State>(State.Loading)  // ✅ Using 'val'
```
