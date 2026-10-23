# গ্রামীণ ব্যাংক কোড সার্চ — Android App Project

এই প্রজেক্টটি আপনার Excel ফাইলের `Code_List` শিট থেকে 260টি কোড/বিবরণ নিয়ে তৈরি করা হয়েছে।

## সুবিধা
- কোড নম্বর দিয়ে সার্চ
- বিবরণের বাংলা/ইংরেজি অংশ দিয়ে সার্চ
- বাংলা সংখ্যা (যেমন ১৩০৯) ও ইংরেজি সংখ্যা (1309) দিয়ে সার্চ
- অফলাইনে কাজ করে; ইন্টারনেট/লগইন লাগে না
- মোবাইল স্ক্রিনে ব্যবহার উপযোগী

## APK তৈরি করার নিয়ম
1. কম্পিউটারে Android Studio ইনস্টল করুন।
2. Android Studio থেকে **Open** করে এই ফোল্ডারটি খুলুন।
3. Gradle sync শেষ হলে মেনু থেকে **Build > Build APK(s)** নির্বাচন করুন।
4. APK সাধারণত `app/build/outputs/apk/debug/app-debug.apk`-এ পাওয়া যাবে।
5. APK ফোনে পাঠিয়ে ইনস্টল করতে পারবেন। Android ইনস্টল করার অনুমতি চাইতে পারে।

## কোড তালিকা আপডেট
`app/src/main/assets/codes.json` ফাইলে কোড ও বিবরণ আছে। Excel ফাইল বদলালে এই JSON ফাইলও আপডেট করতে হবে।

নোট: এই ZIP-এ Android Studio-র source project দেওয়া আছে; এখানে সরাসরি তৈরি করা signed APK অন্তর্ভুক্ত নেই।

শুধু মোবাইল দিয়ে APK বানানোর বিকল্প পদ্ধতি (GitHub Actions):
১) GitHub-এ সাইন ইন/অ্যাকাউন্ট খুলুন এবং একটি নতুন repository তৈরি করুন।
২) ZIP ফাইলটি মোবাইলে Extract করে ভেতরের ফাইলগুলো repository-র main/master branch-এ আপলোড করুন। .github ফোল্ডারটিও আপলোড করতে হবে।
৩) repository-তে Actions ট্যাবে যান। “Build Android APK” workflow বেছে “Run workflow” চাপুন।
৪) কাজ সফল হলে ওই workflow run খুলে Artifacts অংশ থেকে “Grameen-Code-Search-APK” ডাউনলোড করুন। ZIP artifact Extract করে app-debug.apk ইনস্টল করুন।
নোট: GitHub-এ ফাইল আপলোড করার মোবাইল UI পরিবর্তিত হতে পারে। APK এখনো তৈরি করা হয়নি; workflow চালালে ক্লাউডে তৈরি হবে।
