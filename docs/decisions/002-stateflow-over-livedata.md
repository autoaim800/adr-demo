# ADR-002: StateFlow over LiveData

## Decision
Migrate all UI state from LiveData to StateFlow.

## Context
**Approved:**
```kotlin
private val _state = MutableStateFlow<State>(State.Loading)
val state: StateFlow<State> = _state.asStateFlow() // must turn mutable state flow to readonly state flow via .asStateFlow()

// Updates via .value or .update {}
```

**Forbidden**
```kotlin
private val _state = MutableLiveData<State>()
val state: LiveData<State> = _state
```
