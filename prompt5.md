DATABASE, MIGRATION, PURGE AND PERSISTENCE AUDIT
PATHS

.NET PROJECT ROOT:

<ENTER_ABSOLUTE_PATH_TO_DOTNET_PROJECT>

JAVA PROJECT ROOT:

<ENTER_ABSOLUTE_PATH_TO_JAVA_PROJECT>

MIGRATION AUDIT DIRECTORY:

<ENTER_ABSOLUTE_PATH_TO_EXISTING_MIGRATION_AUDIT_DIRECTORY>
EXISTING AUDIT DOCUMENTS

Read:

01_PROJECT_INVENTORY.md
02_DOTNET_TO_JAVA_TRACEABILITY.md
03_GAP_REGISTER.md
04_UNKNOWN_REGISTER.md
05_MIGRATION_AUDIT_SUMMARY.md
06_BUSINESS_LOGIC_DEEP_AUDIT.md
07_API_INTERFACE_AUDIT.md
TASK

Perform a complete database and persistence equivalence audit.

This is a critical audit stage because the application is responsible for database migration and database lifecycle management.

Do not limit this audit to ORM entities or repositories.

Audit the complete database lifecycle behavior.

1. DATABASE SCHEMA

Compare:

databases
schemas
tables
columns
data types
lengths
precision
scale
nullability
defaults
primary keys
foreign keys
unique constraints
indexes
sequences
identity/auto-increment
views
stored procedures
functions
triggers
2. DATABASE CREATION

Compare:

database creation
database existence checks
initialization
initial schema
initial data
permissions
initialization ordering
failure handling
retry behavior
3. MIGRATION ENGINE

Compare:

migration discovery
migration version detection
current version
target version
version comparison
migration selection
migration ordering
migration dependencies
migration preconditions
migration execution
migration scripts
SQL
data transformation
migration metadata
migration history
migration state
completion state
4. MIGRATION FAILURE/RECOVERY

Compare:

transaction boundaries
commit
rollback
partial migration
failed migration state
retry
resume
recovery
idempotency
already-applied migration
duplicate migration execution
database locking
concurrent migration attempts
5. DATA TRANSFORMATION

Compare:

column transformations
data conversions
default values
null handling
date/time conversion
timezone
precision
rounding
string conversion
enum/status conversion
old-to-new data mapping
existing-data handling
6. PURGING

Compare:

purge selection criteria
retention period
age calculation
cutoff calculation
deletion conditions
table ordering
parent/child deletion
referential integrity
batch size
batching
pagination
duplicate handling
empty result behavior
partial purge
transaction behavior
purge retry
purge recovery
purge completion state
7. CLEANUP / ARCHIVAL

Where applicable compare:

cleanup rules
archival
temporary data removal
obsolete data removal
historical data handling
retention policy
cleanup scheduling
8. QUERIES

Compare:

SELECT
INSERT
UPDATE
DELETE
joins
filters
ordering
grouping
aggregation
pagination
projections
batch SQL
native SQL
generated SQL where behaviorally relevant
9. TRANSACTIONS

Compare:

transaction boundaries
isolation
locking
commit
rollback
nested transactions
partial failure
concurrency
deadlock behavior
10. CONNECTION/FAILURE BEHAVIOR

Compare:

connection failures
timeout
pool behavior
unavailable database
invalid credentials
constraint violation
duplicate data
missing data
deadlock
SQL failure
11. MIGRATION SCRIPTS

Inspect actual:

SQL migration files
scripts
version files
migration metadata
stored procedures
database functions
triggers
schema-management tooling

Do not assume equivalent behavior because both applications use the same database technology.

Do not execute destructive database operations.

If runtime verification is required, use only approved safe environments.

Create:

08_DATABASE_PERSISTENCE_AUDIT.md

Update:

03_GAP_REGISTER.md
04_UNKNOWN_REGISTER.md
05_MIGRATION_AUDIT_SUMMARY.md

For every confirmed gap provide exact evidence.

Final response must include:

schema areas compared
migration mechanisms compared
migration scripts compared
purge behavior compared
cleanup/retention behavior compared
data transformation compared
transaction behavior compared
rollback/recovery compared
retry/resume compared
locking/concurrency compared
confirmed gaps
unknowns
runtime evidence
areas not verifiable
confirmation that no source/test/config/database/deployment changes were made
