---
name: database-development
description: Apply Fiascko's database development practices when designing, reviewing, querying, or modifying databases, emphasizing data safety, simple schemas, query performance, and controlled changes.
metadata:
  author: Fiascko
---

# Database Development

Apply these database-specific guidelines alongside `fiascko-philosophy` when working with databases.

## Architecture & Design

- Prefer simple, maintainable database structures that meet actual project requirements.
- Respect the existing database engine, schema, naming conventions, and architecture.
- Avoid unnecessary tables, collections, relationships, indexes, and abstractions.
- Use appropriate data types, constraints, and relationships to maintain data integrity.
- Normalize relational schemas when beneficial without introducing unnecessary complexity.
- Avoid speculative schema changes and premature optimization.

## Queries

- Write clear, readable, and efficient queries.
- Prefer parameterized queries over dynamically constructed SQL.
- Retrieve only the data and columns required for the task.
- Avoid unnecessary joins, subqueries, and repeated database operations.
- Use indexes when justified by actual query patterns and performance needs.
- Consider query execution plans before introducing complex optimizations.

## Data Safety

- Only execute SELECT queries that are verified to be read-only and free of side effects.
- Never execute data-modifying or schema-changing operations, including INSERT, UPDATE, DELETE, DROP, TRUNCATE, ALTER, CREATE, and MERGE.
- Never execute stored procedures, functions, or commands that may modify data or database structures.
- Never bypass these restrictions, even with explicit approval.
- Provide modification queries for manual review and execution only when explicitly requested.
- Treat production databases and unknown environments as sensitive by default.
- Never assume a backup exists.

## Schema Changes & Migrations

- Analyze the existing schema and dependencies before proposing changes.
- Preserve existing data, relationships, constraints, and application compatibility.
- Prefer small, incremental, and reversible migrations when possible.
- Identify potentially destructive or irreversible changes before implementation.
- Consider data migration and rollback requirements when modifying schemas.
- Never execute migrations; provide migration scripts for manual review and execution only.

## Transactions & Reliability

- Design related write operations to use transactions when atomicity is required, without executing them.
- Ensure appropriate rollback behavior when operations fail.
- Respect database constraints and referential integrity.
- Handle database errors and invalid states appropriately.
- Avoid unnecessary locks and long-running transactions.
- Consider concurrency and consistency when relevant.

## Security & Access

- Never expose database passwords, connection strings containing secrets, or credentials.
- Prefer environment variables or secure configuration mechanisms for credentials.
- Only access databases using credentials with read-only permissions.
- Avoid accessing sensitive records unless necessary for the task.
- Never display or export sensitive database contents unnecessarily.
- Access only explicitly authorized databases.

## Performance

- Optimize queries based on actual usage and measured performance.
- Avoid unnecessary database round trips.
- Use pagination or batching for large datasets when appropriate.
- Avoid loading entire datasets into memory without justification.
- Consider index maintenance and write performance before adding indexes.
- Avoid unnecessary caching or complex optimization strategies.

## Verification

- Validate queries and schema changes using available tools when possible.
- Prefer non-destructive verification methods.
- Review the expected impact of modification queries before providing them.
- Suggest verification steps for manually executed changes.
- Never claim queries, migrations, or database operations were executed or verified unless they actually were.
