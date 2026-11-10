---
name: unity-development
description: Apply Fiascko's Unity and C# development practices when writing, reviewing, or modifying code, emphasizing simple architecture, serialized references, performance, and Unity best practices.
metadata:
  author: Fiascko
---

# Unity Development

Apply these Unity-specific guidelines alongside `fiascko-philosophy` when working on Unity projects.

## Architecture

- Follow Unity's component-based architecture and lifecycle conventions.
- Prefer small, focused MonoBehaviour components with clear responsibilities.
- Use plain C# classes for logic that does not require Unity functionality.
- Use ScriptableObject for shared configuration or reusable asset-based data when appropriate.
- Prefer composition and existing components over unnecessary inheritance or new systems.
- Avoid unnecessary managers, singletons, interfaces, and generic architectures.
- Keep implementations proportional to actual project requirements.

## References & Serialization

- Prefer `[SerializeField] private` for Inspector-configured references and values.
- Prefer explicit Inspector references over runtime scene searches.
- Avoid `GameObject.Find`, `FindFirstObjectByType`, and similar searches when direct references are available.
- Use `GetComponent` or `TryGetComponent` for local component access when appropriate.
- Cache frequently accessed references instead of repeatedly resolving them.
- Serialize only necessary Inspector configuration and Unity-serialized data; avoid serializing derived or cached values.
- Avoid unnecessary public fields and serialized members.
- Preserve existing Inspector assignments, serialized names, and asset references.
- Use Unity serialization migration mechanisms when renaming serialized fields is necessary.

## Performance

- Minimize allocations and expensive operations in frequently executed code.
- Avoid repeated scene searches, unnecessary polling, and redundant calculations.
- Prefer event-driven updates when they simplify the implementation.
- Avoid unnecessary LINQ, closures, and temporary collections in performance-sensitive code.
- Use object pooling only when repeated instantiation creates a meaningful cost.
- Avoid excessive logging in frequently executed methods.
- Profile performance issues before introducing complex optimizations.

## Lifecycle

- Use `Awake`, `Start`, `OnEnable`, and `OnDisable` according to their lifecycle responsibilities.
- Use `Update` for frame-based logic and `FixedUpdate` for physics-related updates.
- Use `Time.deltaTime` for frame-rate-independent behavior when appropriate.
- Avoid depending on unspecified execution order between components.
- Manage event subscriptions and resource cleanup consistently.
- Respect Unity object lifetimes and destroyed-object behavior.

## C# Conventions

- Use PascalCase for classes, methods, and properties.
- Use camelCase for local variables and parameters.
- Use `_camelCase` for private fields.
- Keep conditions, method signatures, and calls on one line when reasonably readable.
- Prefer constants for meaningful fixed values and `[SerializeField]` for Inspector-configurable values.
- Prefer built-in Unity and C# functionality over custom implementations.
- Use APIs and language features compatible with the project's Unity version.

## UI & Events

- Update UI when underlying data changes instead of every frame when practical.
- Cache UI references and avoid unnecessary layout rebuilds.
- Subscribe and unsubscribe from events consistently.
- Avoid unnecessary coupling between UI and gameplay components.
- Reuse the project's existing UI system.

## Editor & Runtime

- Keep editor-only functionality separate from runtime code.
- Use `UnityEditor` APIs only in editor-compatible assemblies or conditional compilation.
- Avoid introducing runtime overhead for editor-only functionality.
- Prefer Unity's existing Editor APIs over custom tooling when sufficient.

## Safety & Compatibility

- Validate required Inspector references and handle missing components appropriately.
- Avoid excessive defensive checks for guaranteed internal states.
- Preserve scene, prefab, ScriptableObject, and serialized asset compatibility.
- Avoid changing public APIs or serialized structures without justification.
- Respect Unity's main-thread requirements.
- Do not introduce packages, plugins, or external dependencies without approval.

## Verification

- Check compilation errors and relevant Unity warnings when tools are available.
- Verify serialized references and Inspector configurations when the relevant Unity assets or Editor are accessible.
- Identify any required Inspector assignments after code changes.
- Suggest focused Play Mode or Editor verification when direct execution is unavailable.
- Never claim Unity compilation or runtime behavior was verified without performing the corresponding checks.
