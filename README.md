# Foundation

**A reusable starting point for custom web applications**

Foundation is the application base I have developed and refined over years of building custom websites and business applications. Its purpose is straightforward: provide the common functionality I am likely to need on a new project so I can concentrate on the functionality that makes that project unique.

Foundation is not an open-source framework. The production source code is proprietary and is **not included in this repository**. This repository documents the architecture, purpose, and evolution of the system.

## Core capabilities

### Customer accounts

Many of the applications I build require some form of customer or user account. Foundation provides that starting point, including:

- Customer records and contact information
- Customer authentication and sign-in
- Customer profile maintenance
- An authenticated customer area that can be extended with project-specific functionality

In Foundation itself, the customer-facing functionality is intentionally limited. Individual applications extend the customer area with whatever they require, such as orders, subscriptions, reservations, saved information, or application-specific data.

### Content and page management

Foundation includes a lightweight content-management system for routine site content:

- Create and edit content pages
- Manage site content through the administrative area
- Mark pages as restricted
- Require an authenticated customer account to view restricted content

It is deliberately simple, providing the basic content functionality many projects need without imposing a large CMS on the application.

### Application settings and system email

Foundation also provides common administrative functionality, including:

- Application settings
- Management of system-generated email
- Administrative tools used by the underlying application

These capabilities provide a consistent base that can be extended as a project's requirements grow.

## How I use Foundation

Foundation is a starting point, not the finished application.

```text
                                FOUNDATION
                                    |
          +-------------------------+-------------------------+
          |                         |                         |
   Customer Accounts       Content Management      Application Management
   - Contact info          - Content pages         - Settings
   - Authentication        - Restricted pages      - System email
   - Customer login
          |                         |                         |
          +-------------------------+-------------------------+
                                    |
                         Common Application Base
                                    |
          +-------------------------+-------------------------+
          |                         |                         |
     trinthlo.com           book.trinthlo.com             Maisie's
     Professional            Novel-management          Full e-commerce
       website                 application               application
```

The value of the approach is that the common pieces do not need to be reinvented for every project. Project-specific business rules and features are then developed on top of that base.

## Applications built from Foundation

### trinthlo.com

A professional website built on the Foundation base, using the common application and content-management functionality.

### Books

A specialized web application for managing novels. Foundation supplies the common application structure and account functionality; the novel-management features are application-specific additions.

### Maisie's

A full e-commerce application built outward from Foundation. The common base is extended with the product, shopping, checkout, order, payment, and other commerce functionality required by the application.

These projects illustrate the reason Foundation exists: the same common starting point can support very different applications without making their business logic part of Foundation itself.

## Technical structure

The current Foundation codebase is a ColdFusion/CFML application with a structured separation of application concerns, including controllers, data-access objects, models, validation, views, utilities, configuration, and application assets.

The implementation has evolved over time as I have reused it on new projects and refined the common functionality.

## Further reading

- [Architecture overview](docs/architecture.md)
- [Projects built from Foundation](docs/projects-built-with-foundation.md)

## Source availability

Foundation is part of my private development toolkit. Its production source code and implementation details are not published in this repository.

Public code examples may be provided separately where they can demonstrate individual techniques without exposing Foundation or client source code.

## About

I am a senior web developer with decades of experience building and maintaining custom websites and business applications, with particular experience in ColdFusion/CFML, SQL Server, e-commerce, payment processing, third-party integrations, and legacy application modernization.

More information: [trinthlo.com](https://trinthlo.com)
