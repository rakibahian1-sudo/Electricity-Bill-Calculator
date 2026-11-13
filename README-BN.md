# Electricity Bill Calculator — Android APK

এই প্রজেক্টে আপনার HTML ক্যালকুলেটরটি Android WebView-এর ভিতরে রাখা হয়েছে।
HTML ফাইলটি অ্যাপের ভেতরেই bundled, তাই ক্যালকুলেটর চালাতে ইন্টারনেট লাগবে না।

## GitHub দিয়ে APK তৈরি (Android Studio ছাড়াই)

1. ZIP ফাইলটি Extract করুন।
2. GitHub-এ লগইন করে **New repository** তৈরি করুন, নাম দিন `ElectricityBillCalculator`।
3. Repository-টি **Public** রাখলে GitHub Actions ব্যবহার সহজ হবে।
4. Extract করা ফোল্ডারের ভেতরের সব ফাইল repository-তে upload করুন। `.github` ফোল্ডারটিও অবশ্যই upload করতে হবে।
5. GitHub repository-তে **Actions** tab খুলুন।
6. `Build Android APK` workflow নির্বাচন করে **Run workflow** চাপুন। প্রথম push-এ workflow নিজে থেকেও চলতে পারে।
7. Build শেষ হলে workflow run খুলুন।
8. নিচে **Artifacts** থেকে `Electricity-Bill-Calculator-APK` ডাউনলোড করুন।
9. ZIP artifact Extract করে `app-debug.apk` ফোনে পাঠিয়ে install করুন।
10. Android চাইলে Settings থেকে ওই source-এর app install করার অনুমতি দিন।

## Offline এবং ডেটা

- HTML ফাইলটি APK-র মধ্যে থাকে; প্রথমবার চালাতেও ইন্টারনেট দরকার নেই।
- JavaScript, হিসাব, LocalStorage history ডিভাইসেই চলে।
- অ্যাপ uninstall করলে বা app data মুছলে history হারাতে পারে।
- Print / PDF বাটন Android Print service ব্যবহার করে।

## গুরুত্বপূর্ণ

- এটি debug APK; নিজের ফোনে পরীক্ষা করার জন্য।
- Play Store-এ প্রকাশ করতে হলে release signing, privacy policy এবং Play Console-এর শর্ত আলাদাভাবে পূরণ করতে হবে।
- বিদ্যুৎ ইউনিটের রেট HTML ফাইলে যেমন আছে তেমনই রাখা হয়েছে; সরকারি রেট বদলালে HTML-এ আপডেট করতে হবে।
