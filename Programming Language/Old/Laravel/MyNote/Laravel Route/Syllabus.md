Laravel Route(kamal1974srdi@gmail.com-Laravel Dynamic Parameter)
### **১. প্রাথমিক স্তর (Basic Level)**

**a. বেসিক রাউটিং:**
   - রাউট কী এবং এর কাজ
   - HTTP Methods: `GET`, `POST`, `PUT`, `DELETE` রাউট
   - রাউট এবং ক্লোজার
   - রাউট এর URL এবং ভিউ-এর সংযোগ
   - রাউট প্যারামিটার:
     - **Required Parameters:** `/user/{id}`
     - **Optional Parameters:** `/user/{name?}`
   - Route Priority: Laravel রাউট প্রায়োরিটি কিভাবে নির্ধারণ করে।

**b. Named Routes:**
   - Named Route কী এবং কিভাবে নামকরণ করা হয়
   - Named Route ব্যবহার করে URL তৈরি করা
   - Named Route ব্যবহার করে Redirect করা

**c. Route Redirection:**
   - `Route::redirect()` এর ব্যবহার
   - `Route::permanentRedirect()`

**d. HTTP Verb Constraints:**
   - নির্দিষ্ট HTTP মেথডের উপর ভিত্তি করে রাউট নিয়ন্ত্রণ।

**e. Custom 404 Error for Routes:**
   - কাস্টম 404 পেজ তৈরি এবং Route::fallback()।

---

### **২. মধ্যম স্তর (Intermediate Level)**

**a. রাউট গ্রুপিং (Route Grouping):**
   - রাউট গ্রুপ করার সুবিধা
   - Common Middleware, Prefix, এবং Namespace ব্যবহার
   - গ্রুপ রাউটের মধ্যে প্যারামিটার পাস করা

**b. Middleware:**
   - Middleware কী এবং কেন ব্যবহার করা হয়
   - Route এবং Group-এ Middleware প্রয়োগ
   - Custom Middleware তৈরি এবং ব্যবহার

**c. Route Model Binding:**
   - **Implicit Binding:** মডেলের ID প্যারামিটার হিসেবে গ্রহণ করা
   - **Explicit Binding:** কাস্টম লজিক অনুযায়ী মডেল ফেচ করা

**d. রাউট ফিল্টারিং (Route Filtering):**
   - `where` মেথড ব্যবহার করে রাউট প্যারামিটার ফিল্টার করা
   - Regular Expressions দিয়ে রাউট প্যারামিটার ভ্যালিডেশন

**e. Localized Routes:**
   - একাধিক ভাষার জন্য রাউট তৈরি (Locale-based routing)।
   - URL-এ ভাষা সংযোগ করে কনটেন্ট ডাইনামিক করা।

**f. Controller Routing:**
   - রাউট সরাসরি ক্লোজারের পরিবর্তে কন্ট্রোলারের মেথডের মাধ্যমে পরিচালনা।
   - Single Action Controllers এবং এদের ব্যবহার।

---

### **৩. উচ্চতর স্তর (Advanced Level)**

**a. রিসোর্স রাউট (Resource Routes):**
   - Resource Controller এবং Resource Route এর ব্যবহার
   - Resource Controller এর সাতটি ডিফল্ট মেথড (`index`, `create`, `store`, `show`, `edit`, `update`, `destroy`)
   - Nested Resources

**b. রাউট ম্যাক্রোস (Route Macros):**
   - Route Macros কী এবং কিভাবে তৈরি করা হয়
   - Custom Route Macros তৈরি

**c. রাউট প্রিফিক্স (Route Prefixing):**
   - Route Prefix ব্যবহার করে রাউট গুলিকে একটি সাধারণ URL path-এর অধীনে রাখা
   - Subdomain রাউটিং

**d. API Routing:**
   - API Routes এবং কিভাবে ওয়েব ও API রাউট আলাদা করা হয়
   - API Resource Routes তৈরি করা
   - Rate Limiting প্রয়োগ

**e. Complex Route Constraints:**
   - একাধিক কন্ডিশনের উপর ভিত্তি করে রাউট প্যারামিটার নিয়ন্ত্রণ করা।
   - প্যারামিটারের উপর ভিত্তি করে অ্যালগরিদমিক রাউটিং বাস্তবায়ন।

**f. Route Caching with Custom Routes:**
   - রাউট ক্যাশ এবং কাস্টম রাউট ক্যাশিংয়ের প্রয়োজনীয়তা।
   - বড় অ্যাপ্লিকেশনে পারফরম্যান্স ইম্প্রুভমেন্টের জন্য রাউট ক্যাশের ব্যবহার।

**g. Subdomain Routing with Dynamic Parameters:**
   - সাবডোমেইনভিত্তিক রাউটিং যেখানে ডাইনামিক প্যারামিটার থাকে।

---

### **৪. প্রফেশনাল স্তর (Professional Level)**

**a. রাউট কাস্টমাইজেশন:**
   - কাস্টম প্যারামিটার রেজোলভার তৈরি
   - Route Caching এবং এর পারফরম্যান্স ইম্প্রুভমেন্ট

**b. রাউট ইভেন্টস:**
   - রাউট ইভেন্টস কীভাবে কাজ করে (e.g., `Route::before` এবং `Route::after`)

**c. রাউট ভেরসনিং (Versioning):**
   - API রাউটের ভেরসনিং কৌশল

**d. Route Fallbacks:**
   - `Route::fallback()` এর ব্যবহার
   - 404 পেজ কাস্টমাইজেশন

---

### **৫. অতিরিক্ত বিষয়বস্তু (Optional Topics)**

**a. রাউট ম্যাট্রিক্স এবং স্ট্যাটিসটিক্স:**
   - রাউট পারফরম্যান্স পরিমাপ করা
   - রাউট লগিং এবং মনিটরিং
   
**b. SEO এবং রাউটিং:**
   - SEO বান্ধব রাউট তৈরির কৌশল

**c. Security and Authentication with Routing:**
   - Role-based Access Control (RBAC)
   - Authentication Middleware

**d. Asynchronous Routing Techniques:**
   - Event-driven এবং asynchronous রাউট ব্যবহারের কৌশল, যেমন Queue এবং Broadcasting।
