---
title: Listening for events
weight: 6
---

The package fires events where you can listen for to perform some extra logic.

### `\Spatie\Multitenancy\Events\MakingTenantCurrentEvent`

This event will fire when a tenant is being made the current one. At this point none of [the tasks](/laravel-multitenancy/v1/using-tasks-to-prepare-the-environment/overview/) have been executed. 

It has one public property `$tenant`, that contains and instance of `Spatie\Multitenancy\Models\Tenant`

### `\Spatie\Multitenancy\Events\MadeTenantCurrentEvent`

This event will fire when a tenant has been made the current one. At this point all of [the tasks](/laravel-multitenancy/v1/using-tasks-to-prepare-the-environment/overview/) have been executed. The current tenant will also have been bound as `currentTenant` in the container.

It has one public property `$tenant`, that contains and instance of `Spatie\Multitenancy\Models\Tenant`