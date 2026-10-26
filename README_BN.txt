SKBB Web App V4 — Supabase Connected Starter
=============================================
এটি আগের V2 demo-এর বদলে Supabase Authentication + database ব্যবহার করার Vite project starter।

চালাতে:
1. ZIP extract করুন।
2. Node.js ইনস্টল থাকা কম্পিউটারে project folder খুলুন।
3. Terminal/CMD-তে চালান: npm install
4. .env.example কপি করে .env.local করুন।
5. Supabase Dashboard > Project Settings > API থেকে Project URL ও publishable/anon key বসান।
6. npm run dev চালান, টার্মিনালে দেখানো localhost URL ব্রাউজারে খুলুন।
7. Supabase Authentication user দিয়ে লগইন করুন। profiles table-এ role ও active profile থাকতে হবে।

সতর্কতা:
- Frontend code-এ কখনো service_role/secret key রাখবেন না।
- আপনার আগের SQL schema-তে donors/request/fund/committee tables-এ RLS চালু করা হয়েছিল, কিন্তু সব write/admin policies সম্পূর্ণ নয়। এই app চালানোর আগে policies-কে পূর্ণ ও পরীক্ষিত করতে হবে। নিরাপত্তা যাচাই না হওয়া পর্যন্ত বাস্তব ডোনার/ফান্ডের তথ্য ব্যবহার করবেন না।
- Supabase database schema-এর সাথে field names মিলিয়ে নিতে হবে।
- Committee user creation flow এখনো UI থেকে সম্পূর্ণ হয়নি; Auth user তৈরি ও profile assignment নিরাপদ admin-side process দিয়ে করতে হবে।
- এটি production-ready নয়; security review, robust error handling, audit logs, backups, consent/privacy policies ও role-based write/delete policies যোগ করতে হবে।
