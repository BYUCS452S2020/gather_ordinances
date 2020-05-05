# Ordinance Gather

Gather your deceased ancestors' temple ordinances!

# Project description

Ever wished you could find a relative to take to the temple? Ever thought to yourself, "My Aunt and Grandma have done all our family history! There's noone left who needs their ordinance work done."? Have you ever thought, "I don't have time to do family history work."? If you've ever had any of these thoughts, well, think again! Ordinance Gather seeks to eliminate the complexity and time required to find deceased relatives needing temple work done on their behalf. Once logged in, a user can specify the amount of ordinances that they wish to reserve. Ordinance Gather will then scan their family tree, identifying individuals who need temple work done, and then will automatically reserve the ordinances of that individual, repeating the process until the specified amount of ordinances has been requested. The reserved ordinances will then appear on the users dashboard, with links to Family Search to view more details about them. 

Wtih Ordinance Gather, you'll have hundreds of ordinances gathered in no time!

# Team

I'm looking for one other person to join the team.

# SQL

A PostgreSQL database will be used to store information of each user, the ordinances that they have reserved, and their recent activity.

# No-SQL
A graph-based database, or MongoDB, are possible options.

# Business
This will be offered as a free service to anyone who has an existing FamilySearch account. 

# Legal
The business will be a legal, non-profit 501 (c) Utah organization. All content and ensuing code will become the sole property of Scott Griffin, LLC.

# Technical
- A setup expecting deployment on a linux server. This project will entirely use a test-driven development model

- [Clojure](https://clojure.org/) for server-side/backend development
- [ClojureScript](https://clojurescript.org/) for front-end development.
- [reframe](https://github.com/Day8/re-frame) as a SPA state-management framework upon react.js
- [reitit](https://github.com/metosin/reitit) for front-end and back-end routing
- [cprop](https://github.com/tolitius/cprop/blob/master/README.md) for inclusion of local and environmental variables
- [mount](https://github.com/tolitius/mount) for a component/reloaded workflow
- [hikari-cp](https://github.com/tomekw/hikari-cp) for JDBC database connection pooling 
- [hiccup](https://github.com/weavejester/hiccup) for SSR (server-rendered) base-page
- CSS with [garden](https://github.com/noprompt/garden) and [garden-gnome](https://github.com/Otann/garden-gnome) for hot-reloading as you define your styles as unadorned clojure
- [migratus](https://github.com/yogthos/migratus) for database initialization and migrations
- [figwheel](https://github.com/bhauman/lein-figwheel) for state-preserving hot-reloading of the browser as soon as you save a change in a cljs file

Other configuration based on [luminus](http://www.luminusweb.net/)
