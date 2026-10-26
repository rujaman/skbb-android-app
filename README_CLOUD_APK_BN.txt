SKBB Android APK — Cloud Build Guide (বাংলা)
============================================

এই ZIP-এ APK এখনো নেই। এটি GitHub Actions-এর ফ্রি cloud runner দিয়ে APK build করার workflow যোগ করেছে, তাই আপনার PC-তে Android Studio দরকার নেই।

একবারের সেটআপ:
1. ZIP Extract করুন।
2. GitHub-এ একটি নতুন repository তৈরি করুন (Private রাখাই ভালো)।
3. Extract করা folder-এর সব file GitHub repository-তে upload করুন, .github folder-সহ।
4. GitHub repository-তে Settings/Actions default allow থাকুক।
5. Actions tab খুলুন।
6. বাম পাশের "Build SKBB Android APK" workflow নির্বাচন করুন।
7. "Run workflow" চাপুন।
8. কাজ শেষ হলে সবুজ successful run খুলুন, নিচের Artifacts থেকে "SKBB-debug-APK" ডাউনলোড করুন।
9. ZIP artifact Extract করলে app-debug.apk পাবেন। Android ফোনে পাঠিয়ে install করতে পারবেন (unknown apps install permission চাইতে পারে)।

Supabase config:
- এই workflow build সময় VITE_SUPABASE_URL এবং VITE_SUPABASE_ANON_KEY env variables স্বয়ংক্রিয়ভাবে GitHub-এ সেট করে না।
- Vite build-এ Supabase config লাগলে GitHub repository Settings > Secrets and variables > Actions-এ:
  VITE_SUPABASE_URL
  VITE_SUPABASE_ANON_KEY
  যোগ করুন, এরপর workflow file-এ npm run build step-এর আগে env mapping যোগ করতে হবে। সহজে local .env.local upload করবেন না; এতে public frontend key-ই থাকলেও project details প্রকাশ হতে পারে।
- Publishable key / anon key frontend-এ ব্যবহার করা যায়; কখনো service_role/secret key দেবেন না.
- Current workflow is a debug APK. It is suitable for testing, not Play Store release. Production use requires signed release, security review, tested Supabase RLS and role policies.
