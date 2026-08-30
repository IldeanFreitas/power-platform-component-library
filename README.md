# Power Platform Component Library — Public Reference Case

> **Status: Em evolução.** This repository is a public, vendor-neutral reference
> implementation created for a technical portfolio. It contains no client data,
> production exports, connections, or environment configuration.

## Context

Reusable interface components help Canvas Apps keep a consistent visual language
while keeping navigation, data access, and business rules in the consuming app.
This case demonstrates the design of a configurable application header with
accessible actions and responsive behavior.

## Responsibility

I designed the component contract, variants, accessibility criteria, reference
source, and usage guidance for a reusable Canvas Component pattern.

## What is included

- A generic Power Fx / PaYaml reference component: `src/cmp_app_header.fx.yaml`.
- A documented contract with inputs, events, variants, and boundaries.
- Three usage examples that keep application navigation and state outside the
  component.
- Accessibility and publication-safety guidance.

## Important boundary

This is a **reference source**, not an exported Power Apps application or a
ready-to-import solution. To use it in a real Canvas Component Library, create
the component in Power Apps Studio and validate the generated structure with
`pac canvas pack`. This repository intentionally excludes `.msapp`, Solution,
Flow, connection, tenant, and customer assets.

## Component at a glance

| Item | Value |
|---|---|
| Component | `cmpAppHeader` |
| Type | Canvas Component reference source |
| Variants | `compact`, `default`, `prominent` |
| Themes | `light`, `dark` |
| Dependencies | None; no datasource or connector |
| Accessibility focus | descriptive labels, keyboard order, 44px action targets |

## Repository layout

```text
src/        Reference component source
docs/       Contract and accessibility decisions
examples/   Power Fx usage examples
```

## Evidence and limitations

The repository demonstrates component architecture and documentation practices.
It does not claim production deployment, performance measurements, or business
impact. Any consuming app must validate the source in its own environment and
apply its own design tokens and governance policies.
