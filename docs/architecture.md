# Architecture Overview

Foundation is intentionally a shell for project-specific development rather than a feature-complete product.

## Common layer

The common layer supplies three primary areas:

1. **Customer accounts** — customer/contact records, authentication, sign-in, and profile maintenance.
2. **Content management** — basic page creation and editing, including pages restricted to authenticated customers.
3. **Application management** — shared settings and management of system-generated email.

## Application-specific layer

Features unique to a project are built on top of Foundation rather than added to its common responsibilities. Depending on the application, these can include e-commerce, novel management, reservations, inventory, payments, reporting, or other business-specific workflows.

This separation lets the reusable base remain relatively small, while individual applications can grow substantially without turning every project-specific feature into a Foundation feature.

---

[Back to overview](../README.md) · [Projects built from Foundation](projects-built-with-foundation.md)
