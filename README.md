# Odoo Dependency Graph Generator [![Build Status](https://travis-ci.org/Gimpneek/odoo_dependency_graph.svg?branch=master)](https://travis-ci.org/Gimpneek/odoo_dependency_graph)
A simple script that creates a dependency graph for a given Odoo module. 

# PLEASE NOTE - THIS REPOSITORY IS NO LONGER UNDER ACTIVE DEVELOPMENT

## How it does it
The script fires up ERPPeek and using the ir.module.module & ir.module.module.dependency models creates a hierarchy
graph which can exported via terminal, SVG or JSON.

## Example
This assumes a running Odoo instance at http://localhost:8069 with a database called openerp, logging in as admin:admin as these are defualt settings.
You can supply your own server, database, user and password

```
odoo_dependency_graph web

web
├── base_import
├── board
│   └── hr
├── bus
│   └── im_chat
├── im_odoo_support
├── report
├── web_calendar
├── web_diagram
├── web_gantt
├── web_graph
├── web_kanban
│   ├── base_setup
│   │   └── mail
│   │       ├── email_template
│   │       │   └── auth_signup
│   │       │       └── portal
│   │       ├── fetchmail
│   │       └── share
│   └── web_kanban_gauge
├── web_tests
└── web_view_editor
```

## Road Map
- [x] Add ERPPeek integration to query Odoo instance
- [x] Use Tree structure to handle hierarchy
- [x] Add means to export to JSON
- [ ] Add SVG export
- [ ] Add functionality to add test / coverage metrics to dependencies (Cobertura) 
- [x] Wrap as command line tool
