ধাপে ধাপে Laravel মাইগ্রেশন সিলেবাসকে এমনভাবে সাজানো হয়েছে, যাতে এটি প্রাথমিক থেকে উন্নত ও প্রফেশনাল পর্যায়ের ব্যবহারকারীদের জন্য উপযোগী হয়:

---

### **Laravel Migrations Syllabus (For All Levels)**

#### **প্রাথমিক পর্যায় (Primary Level)**

1. **Introduction to Migrations**
   - **What is Migration?**
   - **Benefits of Migrations**: কেন মাইগ্রেশন গুরুত্বপূর্ণ
   - **Migration Files: Structure and Naming Conventions**: মাইগ্রেশন ফাইল গঠন এবং নামকরণ
   - **Migration vs. Manual Schema Management**: মাইগ্রেশন বনাম ম্যানুয়াল স্কিমা ম্যানেজমেন্ট

2. **Basic Migration Commands**
   - **Creating a Migration**: 
       - `php artisan make:migration` দিয়ে মাইগ্রেশন তৈরি
       - মাইগ্রেশন ফাইলের গঠন
   - **Running Migrations**: 
       - `php artisan migrate` কমান্ড দিয়ে মাইগ্রেশন রান করা
   - **Rolling Back Migrations**: 
       - `php artisan migrate:rollback` দিয়ে মাইগ্রেশন পূর্বাবস্থায় ফেরা
   - **Checking Migration Status**: 
       - `php artisan migrate:status` দিয়ে মাইগ্রেশনের অবস্থা দেখা

3. **Creating and Modifying Database Tables**
   - **Defining Tables and Columns**: টেবিল এবং কলাম তৈরি করা
   - **Basic Column Types**: সাধারণ কলাম টাইপ (string, integer, boolean, etc.)

#### **মাঝারি পর্যায় (Intermediate Level)**

4. **Indexes and Keys**
   - **Creating Indexes**: 
       - `unique()`, `index()`, এবং `primary()` কী ব্যবহার করা
   - **Dropping Indexes and Keys**: 
       - ইন্ডেক্স এবং কী মুছে ফেলার পদ্ধতি

5. **Foreign Key Constraints**
   - **Defining Foreign Keys**: ফরেেন কী কনস্ট্রেইন্ট যুক্ত করা
   - **Cascading Actions**: `onDelete`, `onUpdate` এর ব্যবহার এবং আচরণ

6. **Migration Rollbacks and Steps**
   - **Rolling Back Multiple Migrations**: একাধিক মাইগ্রেশন একবারে রোলব্যাক করা
   - **Rolling Back Specific Steps**: নির্দিষ্ট ধাপে রোলব্যাক করা

7. **Migration Best Practices**
   - **Structuring Migration Files**: ফাইল স্ট্রাকচারিং
   - **Naming Conventions for Migrations**: মাইগ্রেশনের সঠিক নামকরণ
   - **Atomic Migrations**: একক কাজের জন্য প্রতিটি মাইগ্রেশন

#### **উন্নত পর্যায় (Advanced Level)**

8. **Advanced Migration Techniques**
   - **Using Raw SQL in Migrations**: মাইগ্রেশনে Raw SQL ব্যবহারের ক্ষেত্রে
   - **Modifying Columns with `change()`**: `change()` এর মাধ্যমে কলাম পরিবর্তন
   - **Conditional Migrations**: নির্দিষ্ট শর্তের ভিত্তিতে মাইগ্রেশন রান করা

9. **Database Seeding with Migrations**
   - **Writing Seed Classes**: ডাটা সিডিং এর জন্য সিড ক্লাস লেখা
   - **Running Seeders with Migrations**: মাইগ্রেশন চলাকালীন সিডিং করা

10. **Migration Optimization**
    - **Using `migrate:fresh`**: টেবিল ফ্রেশ করে নতুন করে মাইগ্রেশন রান করা
    - **Running Migrations in Production**: প্রোডাকশনে মাইগ্রেশন করার সেরা পদ্ধতি

#### **প্রফেশনাল পর্যায় (Professional Level)**

11. **Database Version Control with Migrations**
    - **Tracking Schema Changes**: স্কিমা পরিবর্তন ট্র্যাক করা
    - **Handling Migration Conflicts in Teams**: মাইগ্রেশন কনফ্লিক্ট সমাধান

12. **Migrations in Production**
    - **Best Practices for Running Migrations in Production**: প্রোডাকশন মাইগ্রেশন পরিচালনার নিয়ম
    - **Rolling Out Schema Changes Safely**: নিরাপদে স্কিমা পরিবর্তন করা

13. **Testing with Migrations**
    - **Using `migrate:fresh` in Tests**: টেস্টে মাইগ্রেশন ফ্রেশ করা
    - **Writing Unit Tests for Migrations**: মাইগ্রেশনের জন্য ইউনিট টেস্ট লেখা

14. **Laravel Migrations and Multi-tenancy**
    - **Managing Multi-tenant Schema Changes**: মাল্টি-টেন্যান্সিতে স্কিমা পরিবর্তন পরিচালনা
    - **Running Migrations for Each Tenant**: প্রতিটি টেন্যান্টের জন্য আলাদা মাইগ্রেশন চালানো

---

এভাবে সিলেবাসটিকে প্রাথমিক, মাঝারি, উন্নত এবং প্রফেশনাল লেভেলে ভাগ করা হয়েছে। প্রাথমিক পর্যায়ে নতুন শিক্ষার্থীদের জন্য বেসিক বিষয়গুলো ফোকাস করা হয়েছে, মাঝারি এবং উন্নত পর্যায়ে যাদের কিছু অভিজ্ঞতা আছে তাদের জন্য গভীর বিষয়গুলো অন্তর্ভুক্ত করা হয়েছে, এবং প্রফেশনাল লেভেলে প্রোডাকশন এবং টেস্টিংয়ের উপর ফোকাস দেওয়া হয়েছে।
