# Case study: reusable Canvas App header

**Status:** Em evolução — public reference implementation.

## Context

Canvas Apps often repeat navigation and user-action patterns across screens.
This reference case explores a reusable header that centralizes the visual
contract while keeping application data, navigation, and business rules in the
parent app.

## Responsibility

I defined the public-safe component contract, responsive variants, event
boundaries, accessibility criteria, reference source, and usage documentation.

## Solution

`cmpAppHeader` is a Canvas Component reference with configurable name, theme,
accent color, compact/default/prominent variants, notification state, and
parent-owned actions. It deliberately has no datasource, connector, tenant,
navigation, or global-state dependency.

## Evidence

- [Component contract](component_contract.md)
- [Accessibility decisions](accessibility.md)
- [Power Fx usage examples](../examples/usage.md)
- [Reference source](../src/cmp_app_header.fx.yaml)

## Limitations

The repository does not include an exported `.msapp` or a Solution. A consumer
must recreate the component in Power Apps Studio and validate its generated
source with the supported Power Platform CLI before release. No performance,
production, or business-impact result is claimed here.

## Technologies

Power Apps Canvas Components, Power Fx, PaYaml reference structure,
accessibility-focused UI design, and Git-based documentation.
