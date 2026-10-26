SKBB Android APK Starter — বাংলা নির্দেশনা
===========================================

এই প্যাকেজটি V6 ওয়েব অ্যাপকে Android APK বানানোর জন্য Capacitor config যোগ করে। APK এখনই তৈরি করা হয়নি।

প্রথমে:
1. ZIP Extract করুন।
2. .env.example কপি করে .env.local বানান।
3. VITE_SUPABASE_URL ও VITE_SUPABASE_ANON_KEY-এ নিজের Supabase Project URL এবং Publishable key বসান। Secret/service_role key ব্যবহার করবেন না।
4. এই ফোল্ডারে Address Bar-এ cmd লিখে Enter চাপুন।
5. চালান:
   npm install
   npm run build
   npx cap add android
   npx cap sync android
   npx cap open android

প্রয়োজন:
- Windows-এ Android Studio ইনস্টল থাকতে হবে।
- Android Studio থেকে Android SDK ইনস্টল থাকতে হবে।
- Android Studio-তে Gradle sync শেষ হলে Build > Build Bundle(s) / APK(s) > Build APK(s) নির্বাচন করুন।
- APK সাধারণত android/app/build/outputs/apk/debug/app-debug.apk-এ তৈরি হবে।

যদি `npx cap add android` বলে platform already exists, তাহলে ওই ধাপ বাদ দিয়ে `npx cap sync android` চালান।
যদি JDK/SDK/Gradle error হয়, error text কপি করে দিন।

গুরুত্বপূর্ণ:
- এটি APK তৈরির starter; এই ZIP-এ তৈরি করা APK নেই।
- Supabase URL/key ঠিক না থাকলে বা database policies অসম্পূর্ণ হলে app-এর data features কাজ নাও করতে পারে।
- বাস্তব donor/patient/financial data ব্যবহারের আগে authentication, RLS policies, role permissions ও backup যাচাই করুন।
