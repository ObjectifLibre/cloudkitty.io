---
layout: post
title: Catnip v0.1.0
tags: [Blog, Annoucement]
thumbnail: /assets/catnip-release/thumbnail.png
---

<p align="center">
    <img width="200" src="assets/catnip-release/catnip_logo.png"/>
</p>

The first version of **Catnip** is officially here! Most of you may not know
what Catnip is and that's why we are making this post today.

## What is Catnip ?

Catnip is a dashboard for **Cloudkitty**. This dashboard can be used for
standalone CloudKitty deployments, outside of an Openstack environment. The
existing dashboard [cloudkitty-dashboard](https://github.com/openstack/cloudkitty-dashboard)
is an Horizon (OpenStack's dashboard) plugin, which is why it cannot be
used outside of an OpenStack context.

With Catnip, operators can easily define rating policies for their cloud
without the use of a command line client. Users can get information about
their usage, and predict costs of an instance.

The project is open-source and you're welcome to contribute! You can find the code [here](https://github.com/ObjectifLibre/catnip).

## What's the main benefit ?

CloudKitty's Horizon plugin is very limited due to Horizon restrictions. Its
purpose is simply a fast overview of the estimated costs of your resources
without requiring the CLI. In addition, cloudkitty-dashboard is still using v1
cloudkitty-api version, meaning that it cannot benefit from new API features.

Catnip aims at taking advantage of all the features provided by Cloudkitty:

 - View on all elements : Summary, Scopes, Hashmap...
 - Dynamic summary charts
 - Custom report filtering and grouping

## Catnip views

Catnip gives you access to all CloudKitty elements in separate views,
listed in the navigation bar.

### Summary and Charts

**Summary** and **Summary-Charts** are non-admin views, similarly as in Horizon.
Every registered user can see the estimated cost for his resources and apply
custom filters to the available summaries.

Catnip provides interfaces allowing to add filters and query parameters to
refine the information you're looking for. User can modify their requests with
the following tools:
 - Group By
 - Key-Value filters
 - Timeframes
 - Thresholds (for charts): allows to change a chart's granularity.

<p align="center">
    <img width="900" src="assets/catnip-release/summary-charts.png"/>
</p>
<p align="center">
    <i>Summary-Charts web interface</i>
</p>

### Rating Modules

**Rating Modules** is an admin view. It shows CloudKitty's rating modules:
 - noop: Rating module for testing purpose (enabled only).
 - hashmap: Default rating module corresponding to usual CloudKitty use cases (disabled by default).
 - pyscripts: Custom rating module allowing you to add your own python scripts (disabled by default).

 The view allows to enable and disable modules, and to change their granularity.

<p align="center">
    <img width="900" src="assets/catnip-release/rating-modules.png"/>
</p>
<p align="center">
    <i>Rating Modules web interface</i>
</p>

### Hashmap rating module

**Hashmap** is an admin view. It provides an overview of the objects
representing the rules defined in the HashMap rating module:

 - Services
 - Groups
 - Fields
 - Mappings
 - Thresholds

If you want more informations on the HashMap rating module and its resources,
check out the [hashmap documentation](https://docs.openstack.org/cloudkitty/latest/user/rating/hashmap.html)

In order to get a better overview of the relations between the different
resources, there's a nested representation in Catnip. Users can create and
update all HashMap objects and rating rules with Catnip.

<p align="center">
    <img width="900" src="assets/catnip-release/hashmap.png"/>
</p>
<p align="center">
    <i>Hashmap web interface</i>
</p>


### Scopes

**Scopes** is an admin view. It lists the status of the scopes CloudKitty is
processing.

It is possible to filter on every attribute a scope is made of, that is:
 - Fetcher
 - Collector
 - Scope ID
 - Scope Key

Check [CloudKitty’s architecture documentation](https://docs.openstack.org/cloudkitty/latest/admin/architecture.html)
for details about scopes and their attributes.

<p align="center">
    <img width="900" src="assets/catnip-release/scopes.png"/>
</p>
<p align="center">
    <i>Scopes web interface</i>
</p>

We hope to make you want to try Catnip out and hear from you soon!
