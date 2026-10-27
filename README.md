# Screen Translate & Speak (Android Floating Bubble App)

এই অ্যান্ড্রয়েড অ্যাপ প্রজেক্টটি আপনার স্ক্রিনের যেকোনো অ্যাপ বা ব্রাউজারের ওপর একটি **ফ্লোটিং বাবল (Floating Bubble)** তৈরি করে। বাবলটিতে ট্যাপ করলে এটি স্ক্রিনে থাকা **English, Japanese, এবং Korean** টেক্সট পড়ে সেটিকে **বাংলা (Bengali)** অথবা **হিন্দি (Hindi)** ভাষায় অনুবাদ করে এবং সাথে সাথে **Text-to-Speech (TTS)** এর মাধ্যমে ভয়েসে পড়ে শোনায়।

## ফিচারসমূহ
- **Floating Bubble Overlay (`WindowManager`)**: যেকোনো অ্যাপ বা ব্রাউজারের ওপর ছোট ভাসমান বাবল।
- **Screen Text Extraction (`AccessibilityService` + `takeScreenshot`)**: স্ক্রিনের টেক্সট এবং ছবি/মাঙ্গা/গেমের ভেতরের টেক্সট (Google ML Kit OCR: Latin, Japanese, Korean) শনাক্তকরণ।
- **On-Device Translation (Google ML Kit)**: ইংলিশ, জাপানিজ ও কোরিয়ান থেকে বাংলা এবং হিন্দিতে দ্রুত অনুবাদ।
- **Auto Text-to-Speech (`TextToSpeech`)**: অনুবাদ হওয়ার সাথে সাথে বাংলা (`bn-IN`) ও হিন্দি (`hi-IN`) ভয়েসে পড়ে শোনানোর সুবিধা।

## কিভাবে এই প্রজেক্ট থেকে `.apk` ফাইল তৈরি করবেন (২টি সহজ উপায়)

### উপায় ১: কম্পিউটার ছাড়াই ফোনে বসে GitHub দিয়ে APK ডাউনলোড (সবচেয়ে সহজ)
প্রজেক্টটিতে স্বয়ংক্রিয়ভাবে `.apk` তৈরি করার জন্য `.github/workflows/build_apk.yml` যুক্ত করা আছে:
1. আপনার ফোন বা ব্রাউজার থেকে [GitHub](https://github.com)-এ একটি নতুন Repository তৈরি করুন।
2. এই ZIP ফাইলের ভেতরের সব ফাইলগুলো সেখানে আপলোড করুন।
3. **Actions** ট্যাবে গেলে দেখবেন **Build ScreenTranslateSpeak APK** নিজে থেকেই রান হয়ে গেছে এবং ১-২ মিনিটের মধ্যে রেডিমেড **`ScreenTranslateSpeak-debug-apk`** ডাউনলোডের জন্য তৈরি হয়ে গেছে।

### উপায় ২: Android Studio ব্যবহার করে
1. [Android Studio](https://developer.android.com/studio)-তে প্রজেক্ট ফোল্ডারটি ওপেন করুন।
2. মেনু থেকে **Build ➔ Build Bundle(s) / APK(s) ➔ Build APK(s)** ক্লিক করুন।
3. `app/build/outputs/apk/debug/app-debug.apk` ফাইলটি ফোনে ইনস্টল করুন।
