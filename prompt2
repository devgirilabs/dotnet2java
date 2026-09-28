DEEP BUSINESS LOGIC AND DATABASE LIFECYCLE AUDIT
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
TASK

Perform a deep method-level business logic comparison between the .NET golden/reference application and the Java migration.

For this application, database lifecycle behavior is core business logic.

Therefore explicitly audit every method involved in:

Database migration
migration initiation
migration sequencing
migration version selection
version detection
version comparison
migration ordering
dependency handling
pre-migration checks
migration execution
data transformation
post-migration validation
migration completion
migration state tracking
migration failure
retry
resume
rollback/recovery
Database lifecycle
database creation
database initialization
schema creation
schema upgrades
schema validation
database version tracking
database state transitions
database selection/routing
Purging and cleanup
purge initiation
retention calculation
records selected for purge
filtering rules
deletion ordering
batch size
batch processing
cleanup rules
archival rules
duplicate handling
partial cleanup
retry
resume
cleanup completion
cleanup failure
General business behavior

Also audit:

controllers
services
business services
managers
processors
handlers
workflows
validators
repositories where business behavior depends on them
integrations
messaging
events
background logic
scheduled logic

For every significant method compare:

inputs
outputs
object creation
object mutation
state changes
validation
conditionals
loops
early returns
filtering
sorting
mapping
transformations
calculations
rounding
conversions
strings
null handling
empty handling
default handling
collection behavior
duplicate behavior
ordering
missing-data handling
SQL/database operations
transactions
commit
rollback
locking
concurrency
external calls
request construction
response handling
retry
timeout
exception handling
fallback
configuration
feature flags
authorization
asynchronous behavior
messages/events
state transitions
side effects

Trace:

helper methods
utility classes
base classes
inherited methods
interfaces
implementations
overrides
extension methods
static utilities
callbacks
event handlers
middleware
filters
interceptors
dependency injection
shared modules
SQL scripts
migration scripts
stored procedures/functions/triggers where applicable
REQUIRED SCENARIOS

Check at minimum:

successful migration
migration with existing database
migration from each relevant version
migration with missing/invalid version
migration failure
migration rollback/recovery
migration retry
migration resume
partial migration
schema validation failure
data transformation failure
database connection failure
database timeout
database already exists
database does not exist
successful purge
retention-based purge
empty purge result
partial purge
purge failure
purge retry
duplicate data
missing data
invalid data
concurrent database operation
authorization failure
configuration-dependent behavior
scheduled/background execution

Compare both directions.

Identify:

.NET behavior missing from Java
Java behavior not present in .NET
different behavior
partially migrated behavior
behavior that cannot yet be verified

Create:

06_BUSINESS_LOGIC_DEEP_AUDIT.md

Update:

03_GAP_REGISTER.md
04_UNKNOWN_REGISTER.md
05_MIGRATION_AUDIT_SUMMARY.md

For every confirmed gap include:

Gap ID
category
.NET file/class/method
Java file/class/method
.NET behavior
Java behavior
exact difference
evidence
affected scenario
impact
confidence

Do not fix anything.

Final response must include:

methods examined
database lifecycle methods examined
migration flows examined
purge/cleanup flows examined
Java counterparts
MATCH count
PARTIAL count
MISSING count
DIFFERENT count
UNKNOWN count
confirmed gaps
unknowns
incomplete areas
whether another audit pass is required
confirmation that no source/test/config/dependency/build/database/deployment files were modified
