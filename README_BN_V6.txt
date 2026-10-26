SKBB Web App V6 — Mobile Friendly
==================================
সমাজ কল্যাণ ব্লাড ব্যাংকের responsive web app starter.

মোবাইলে:
- নিচে fixed navigation bar
- দুই কলামের dashboard cards
- বড় touch targets এবং mobile-friendly forms
- ছোট স্ক্রিনে horizontal scroll table
- mobile-friendly modal

ডেস্কটপে:
- sidebar navigation ও full dashboard layout

চালানোর নিয়ম:
1. ZIP Extract করুন।
2. .env.example কপি করে .env.local নাম দিন।
3. .env.local-এ Supabase Project URL ও Publishable key বসান:
   VITE_SUPABASE_URL=https://YOUR_PROJECT_REF.supabase.co
   VITE_SUPABASE_ANON_KEY=sb_publishable_...
   (কখনো service_role/secret key দেবেন না)
4. Command Prompt-এ এই ফোল্ডার খুলে চালান:
   npm install
   npm run dev
5. ব্রাউজারে http://localhost:5173/ খুলুন।

নোট:
- আপনার আগের .env.local ফাইল নিরাপত্তার জন্য ZIP-এ রাখা হয়নি। নতুন ফোল্ডারে নিজে তৈরি করুন।
- এটি আগের V4 codebase-এর mobile responsive update, সম্পূর্ণ feature audit নয়। ডোনার/রোগী/অর্থনৈতিক তথ্যের জন্য production ব্যবহারের আগে Supabase RLS, role permissions, CRUD flows এবং backups পরীক্ষা করতে হবে।
- আপনার আগের ডেটাবেসে committee_member (singular) এবং অন্য টেবিল/কলামের নাম অ্যাপের কোডের সঙ্গে মিলিয়ে নিন।
