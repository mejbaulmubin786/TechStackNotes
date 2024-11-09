Laravel মাইগ্রেশন এর প্রতিটি টপিককে সাব-টপিক আকারে ভাগ করে বিস্তারিত সিলেবাস নিচে দেওয়া হলো:

### Laravel Migrations Syllabus (With Subtopics)

#### 1. **Introduction to Migrations**
   - **1.1** What is Migration?
   - **1.2** Benefits of Migrations
   - **1.3** Migration vs. Manual Schema Management
   - **1.4** Migration Files: Structure and Naming Conventions

#### 2. **Basic Migration Commands**
   - **2.1** Creating a Migration
       - Using `php artisan make:migration`
       - File structure of a new migration
   - **2.2** Running Migrations
       - Using `php artisan migrate`
       - Understanding `up()` and `down()` methods
   - **2.3** Rolling Back Migrations
       - Using `php artisan migrate:rollback`
       - Understanding rollback behavior
   - **2.4** Resetting and Re-running Migrations
       - Using `migrate:reset` and `migrate:refresh`
       - Differences between reset and refresh
   - **2.5** Checking Migration Status
       - Using `migrate:status`
       - Analyzing migration logs

#### 3. **Creating and Modifying Database Tables**
   - **3.1** Defining Tables and Columns
       - Basic syntax for defining tables
       - Common column types (`string()`, `integer()`, `boolean()`, etc.)
   - **3.2** Modifying Existing Tables
       - Adding new columns
       - Removing columns
   - **3.3** Renaming Tables and Columns
       - Using `rename()` for tables and columns
       - Impact of renaming in production environments
   - **3.4** Table Options
       - Setting engine and charset for tables

#### 4. **Indexes and Keys**
   - **4.1** Creating Indexes
       - Defining simple and composite indexes
       - Using `unique()`, `index()`, and `primary()`
   - **4.2** Dropping Indexes and Keys
       - Syntax for dropping indexes
       - Dropping primary keys or foreign key constraints

#### 5. **Foreign Key Constraints**
   - **5.1** Defining Foreign Keys
       - Syntax for adding foreign key constraints
       - Referencing primary keys in other tables
   - **5.2** Relationships and Foreign Keys
       - One-to-One relationships
       - One-to-Many relationships
       - Many-to-Many relationships
   - **5.3** Cascading Actions
       - Setting `onDelete` and `onUpdate` behaviors
       - Managing cascading deletes and updates

#### 6. **Migration Rollbacks and Steps**
   - **6.1** Rolling Back Multiple Migrations
       - Using `migrate:rollback` with multiple steps
   - **6.2** Rolling Back to a Specific Migration
       - Using rollback with step counts (`--step` option)
   - **6.3** Defining `down()` Method for Safe Rollbacks
       - Ensuring proper undo functionality in `down()` methods

#### 7. **Migration Best Practices**
   - **7.1** Structuring Migration Files
       - Separating large migrations into smaller parts
   - **7.2** Naming Conventions for Migrations
       - Using meaningful names based on the table or action
   - **7.3** Keeping Migrations Atomic
       - Ensuring single responsibility for each migration

#### 8. **Advanced Migration Techniques**
   - **8.1** Using Raw SQL in Migrations
       - Executing raw SQL queries for complex schema changes
       - Benefits and risks of raw SQL
   - **8.2** Modifying Columns with `change()`
       - Changing existing columns with `change()`
       - Limitations and alternatives to `change()`
   - **8.3** Conditional Migrations
       - Running migrations conditionally based on environment or settings
   - **8.4** Handling Large Datasets in Migrations
       - Best practices for modifying or migrating large tables

#### 9. **Database Seeding with Migrations**
   - **9.1** Introduction to Seeding
       - Using the `php artisan make:seeder` command
   - **9.2** Writing Seed Classes
       - Populating tables with dummy or initial data
   - **9.3** Running Seeders with Migrations
       - Using `php artisan db:seed` with migrations
   - **9.4** Calling Seeders Automatically
       - Running seeders after specific migrations

#### 10. **Migration Optimization**
   - **10.1** Using `migrate:fresh`
       - Dropping and recreating all tables in one command
   - **10.2** Using `migrate --force` in Production
       - Running migrations in production safely
   - **10.3** Performance Optimization in Large Migrations
       - Techniques to speed up migration execution

#### 11. **Database Version Control with Migrations**
   - **11.1** Tracking Schema Changes
       - Using migration history to track changes across environments
   - **11.2** Handling Migration Conflicts in Teams
       - Merging migration conflicts in version control
   - **11.3** Using Version Control Tools with Migrations
       - Integrating migrations with tools like Git

#### 12. **Migrations in Production**
   - **12.1** Best Practices for Running Migrations in Production
       - Testing migrations before running them on live systems
   - **12.2** Rolling Out Schema Changes
       - Techniques for making schema changes with minimal downtime
   - **12.3** Database Downtime Considerations
       - Planning for minimal downtime during migrations

#### 13. **Testing with Migrations**
   - **13.1** Using `migrate:fresh` in Tests
       - Refreshing the database schema for testing purposes
   - **13.2** Writing Unit Tests for Migrations
       - Testing database schema changes
   - **13.3** Using In-Memory Databases for Testing
       - Configuring in-memory databases for faster test execution

#### 14. **Laravel Migrations and Multi-tenancy**
   - **14.1** Managing Multi-tenant Schema Changes
       - Best practices for handling migrations in multi-tenant apps
   - **14.2** Running Migrations for Each Tenant
       - Automating tenant-specific migrations

এই সিলেবাস অনুযায়ী Laravel মাইগ্রেশন এর সব টপিক এবং সাব-টপিক গুলো সমন্বিত করা হয়েছে, যাতে বিষয়গুলোকে ধাপে ধাপে সহজভাবে আয়ত্ত করা যায়।
