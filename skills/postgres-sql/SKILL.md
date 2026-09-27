---
name: postgres-sql
description: Helps write review optimize and debug SQL queries specifically for PostgreSQL. Use when user mentions Postgres PostgreSQL SQL query SELECT INSERT UPDATE DELETE CTE window functions performance indexing EXPLAIN or asks to generate review fix SQL for PG database.
---

# PostgreSQL SQL Skill

## Overview
Specialized guidance for authoring, reviewing, optimizing, and debugging SQL queries tailored to PostgreSQL's features, best practices, and performance characteristics.

## Instructions
1. Understand requirements: table schemas, data volumes, access patterns, performance goals; request EXPLAIN ANALYZE when available.
2. Write parameterized PostgreSQL SQL. Prefer standard SQL plus appropriate PostgreSQL extensions. Use CTEs for complex logic and PostgreSQL-native JSON, window, date/time, and upsert features where useful.
3. Review correctness, joins, filters, aggregation, subqueries, NULL handling, timezone semantics, Cartesian products, security, maintainability, least privilege, and RLS where applicable.
4. Optimize with EXPLAIN (ANALYZE, BUFFERS, FORMAT JSON); consider appropriate indexes (BTREE, GIN, BRIN), query rewrites, partitioning, materialized views, and statistics.
5. Use PostgreSQL patterns such as ILIKE, DISTINCT ON, ON CONFLICT, LATERAL, keyset pagination, GROUPING SETS/ROLLUP, tsvector/tsquery, and jsonb indexing when appropriate.
6. For errors, diagnose constraint violations, duplicate keys, locking/deadlocks, transaction ordering, and isolation issues; provide corrected SQL.
7. Prefer snake_case identifiers and TIMESTAMPTZ for timezone-aware timestamps. Use transactions for multi-statement changes and VACUUM/ANALYZE where relevant.

## Output requirements
- Put SQL in fenced code blocks with PostgreSQL syntax highlighting.
- Include concise reasoning and testing steps.
- For performance recommendations, distinguish observed plan facts from hypotheses and request plan evidence when absent.
- Assume the latest stable PostgreSQL release unless a version is specified.
