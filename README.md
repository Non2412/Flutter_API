# 🍳 Delicious Recipes - Flutter App

แอปพลิเคชัน Delicious Recipes ที่สร้างด้วย Flutter สำหรับค้นหาและสำรวจสูตรอาหารจากทั่วโลก พร้อมด้วย UI/UX ที่สวยงามและใช้งานง่าย

<div align="center">
  
![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)
![API](https://img.shields.io/badge/API-DummyJSON-orange?style=for-the-badge)

*Discover amazing recipes from around the world* 🌍

</div>

---

## ✨ ฟีเจอร์หลัก

### 🎨 **Modern UI Design**
- **Gradient Background** - พื้นหลังแบบไล่สีสวยงาม
- **Glass Morphism Effects** - เอฟเฟกต์แก้วขุ่นทันสมัย  
- **Smooth Animations** - แอนิเมชันที่ลื่นไหล
- **Responsive Cards** - การ์ดที่ตอบสนองต่อการสัมผัส

### 📱 **User Experience**
- **Intuitive Navigation** - การใช้งานที่เข้าใจง่าย
- **Loading States** - แสดงสถานะการโหลดที่สวยงาม
- **Error Handling** - จัดการข้อผิดพลาดอย่างเหมาะสม
- **Smooth Transitions** - การเปลี่ยนแปลงที่นุ่มนวล

### 🍽️ **Recipe Features**
- **Recipe Cards** - แสดงสูตรอาหารแบบการ์ด
- **Rating System** - ระบบให้คะแนนพร้อมดาว
- **Difficulty Levels** - ระดับความยาก (Easy/Medium/Hard)
- **Time & Servings** - แสดงเวลาและจำนวนผู้ทาน
- **Cuisine Types** - ประเภทอาหารจากหลายประเทศ

### 🌐 **API Integration**
- **Real-time Data** - ข้อมูลสดจาก DummyJSON API
- **Network Error Handling** - จัดการข้อผิดพลาดเครือข่าย
- **Image Loading** - โหลดรูปภาพแบบ Progressive
- **Data Caching** - แคชข้อมูลเพื่อประสิทธิภาพ

---

## 🛠️ เทคโนโลยีที่ใช้

### 🚀 **Core Technologies**
```
Flutter 3.0+    │ Cross-platform framework
Dart 3.0+       │ Programming language  
Material 3      │ Design system
HTTP Package    │ API communication
```

### 📦 **Dependencies**
```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^1.1.0
  
dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.0
```

### 🎯 **Key Packages**
- **http** - สำหรับเรียก REST API
- **dart:convert** - จัดการ JSON data  
- **dart:math** - คำนวณทางคณิตศาสตร์

---

## 📁 โครงสร้างโปรเจค

```
lib/
├── main.dart                 # หน้าหลักและ App entry point
├── models/
│   └── recipe.dart          # Recipe data model
├── services/
│   └── recipes_service.dart # API service layer
├── widgets/
│   ├── recipe_card.dart     # Recipe card component
│   └── loading_widget.dart  # Loading animations
└── screens/
    └── recipes_screen.dart  # Main recipes screen
```

---

## 🚀 การติดตั้งและใช้งาน

### 📋 **ความต้องการระบบ**
- ✅ Flutter SDK 3.0 หรือใหม่กว่า
- ✅ Dart 3.0 หรือใหม่กว่า  
- ✅ Android Studio หรือ VS Code
- ✅ Internet Connection สำหรับ API calls

### ⚡ **ขั้นตอนการติดตั้ง**

1. **Clone Repository**
```bash
git clone <your-repository-url>
cd delicious-recipes-app
```

2. **ติดตั้ง Dependencies** 
```bash
flutter pub get
```

3. **ตรวจสอบการตั้งค่า**
```bash
flutter doctor
```

4. **รันแอปพลิเคชัน**
```bash
flutter run
```

### 🔧 **การตั้งค่าเพิ่มเติม**

**สำหรับ Android:**
```xml
<!-- android/app/src/main/AndroidManifest.xml -->
<uses-permission android:name="android.permission.INTERNET" />
```

**สำหรับ iOS:**
```xml
<!-- ios/Runner/Info.plist -->
<key>NSAppTransportSecurity</key>
<dict>
    <key>NSAllowsArbitraryLoads</key>
    <true/>
</dict>
```

---

## 🎨 Design System

### 🌈 **Color Palette**
```dart
Primary Colors:
├── 🔴 #FF6B6B (Coral Pink)     │ Main brand color
├── 🌸 #FF9A9E (Light Pink)     │ Gradient start  
├── 💜 #FECFEF (Lavender)       │ Gradient middle
└── 🌟 #FFE0E0 (Pale Pink)      │ Gradient end

Accent Colors:
├── 🟢 #4CAF50 (Green)          │ Easy difficulty
├── 🟠 #FF9800 (Orange)         │ Medium difficulty  
├── 🔴 #F44336 (Red)            │ Hard difficulty
└── ⭐ #FFC107 (Amber)          │ Star ratings
```

### 🎭 **Animation Types**
- **Fade Transitions** - การปรากฏแบบค่อยๆ จาง
- **Slide Animations** - การเลื่อนเข้าจากข้าง
- **Scale Effects** - การขยาย/หดขณะแตะ
- **Staggered Loading** - การโหลดแบบเป็นลำดับ

### 📐 **Layout Structure**
```
┌─────────────────────────────────┐
│           App Header            │ <- Gradient + Icon + Title
├─────────────────────────────────┤
│                                 │
│      Recipe Cards List          │ <- Scrollable list
│                                 │ 
│  ┌─────────────────────────┐    │
│  │ [IMG] │ Title          │    │ <- Individual recipe card
│  │       │ Tags • Rating  │    │
│  │       │ Description    │    │
│  │       │ Time • Serving │    │
│  └─────────────────────────┘    │
│                                 │
└─────────────────────────────────┘
```

---

## 🔌 API Integration

### 🌐 **DummyJSON Recipes API**
```
Base URL: https://dummyjson.com/recipes
Method: GET
Response: JSON with recipe array
```

### 📊 **Data Structure**
```json
{
  "recipes": [
    {
      "id": 1,
      "name": "Classic Margherita Pizza",
      "ingredients": ["..."],
      "instructions": ["..."],
      "prepTimeMinutes": 20,
      "cookTimeMinutes": 15,
      "servings": 4,
      "difficulty": "Easy",
      "cuisine": "Italian",
      "rating": 4.6,
      "image": "https://cdn.dummyjson.com/recipe-images/1.webp",
      "tags": ["Pizza", "Italian"]
    }
  ]
}
```

### 🔄 **Service Layer**
```dart
class RecipesService {
  static Future<List<Recipe>> fetchRecipes() async {
    // API call implementation
    // Error handling
    // Data parsing
  }
}
```

---

## 🎯 ฟีเจอร์เด่น

### ✨ **Stunning Visual Effects**

**1. Gradient Backgrounds**
- 4-stop linear gradient สำหรับพื้นหลัง
- Glass morphism effects บนการ์ด
- Shadow effects ที่เปลี่ยนแปลงตาม interaction

**2. Smart Animations**  
- **Staggered animations** - การ์ดปรากฏทีละใบตามลำดับ
- **Hover effects** - การ์ดขยายเมื่อแตะ
- **Loading animations** - Spinner พร้อม gradient background

**3. Interactive Elements**
- **Touch feedback** - การตอบสนองต่อการสัมผัส
- **Color-coded difficulty** - สีที่แตกต่างตามระดับความยาก
- **Rating badges** - ป้ายคะแนนพร้อมดาว

### 📱 **Responsive Design**
- ปรับขนาดตาม screen size
- Touch-friendly button sizes  
- Optimized for both portrait และ landscape
- Cross-platform compatibility (iOS + Android)

---

## 🧩 Component Architecture

### 🏗️ **Widget Structure**
```dart
MyApp                           // Root application
└── RecipesScreen              // Main screen
    ├── Custom Header          // App title + subtitle  
    ├── FutureBuilder         // API data management
    │   ├── Loading State     // Progress indicator
    │   ├── Error State       // Error message
    │   └── Success State     // Recipe list
    └── RecipeCard[]          // Individual recipe cards
        ├── Recipe Image      // Network image + loading
        ├── Recipe Info       // Title, tags, description  
        └── Action Buttons    // Time, servings, favorite
```

### 🎨 **Custom Widgets**
- **RecipeCard** - การ์ดสูตรอาหารแบบ interactive
- **InfoChip** - ชิปแสดงข้อมูล (เวลา, จำนวนคน)  
- **DifficultyBadge** - ป้ายระดับความยาก
- **RatingBadge** - ป้ายคะแนนพร้อมดาว

---

## 🔧 การ Customize

### 🎨 **เปลี่ยนสีธีม**
```dart
// ใน main.dart
ColorScheme.fromSeed(
  seedColor: const Color(0xFFFF6B6B), // เปลี่ยนสีหลัก
  brightness: Brightness.light,       // โหมดสว่าง/มืด
)
```

### 🌈 **ปรับ Gradient**
```dart
// ใน RecipesScreen
const BoxDecoration(
  gradient: LinearGradient(
    colors: [
      Color(0xFFFF9A9E),  // สี 1
      Color(0xFFFECFEF),  // สี 2  
      Color(0xFFFFE0E0),  // สี 3
    ],
  ),
)
```

### ⚙️ **เปลี่ยน API Endpoint**
```dart
// ใน RecipesService
static const String apiUrl = 'https://your-api.com/recipes';
```

---

## 🐛 การแก้ไขปัญหา

### ❌ **ปัญหาที่พบบ่อย**

**1. Network Error**
```
Solution: ตรวจสอบ Internet connection และ API endpoint
```

**2. Image Loading Issues**  
```
Solution: ใช้ errorBuilder และ loadingBuilder
```

**3. Performance Issues**
```
Solution: ใช้ ListView.builder แทน ListView
```

### 🔍 **Debug Tips**
```dart
// Enable HTTP logging
import 'dart:developer' as developer;

developer.log('API Response: $responseBody');
```

---

## 📈 การปรับปรุงในอนาคต

### 🚀 **Planned Features**
- [ ] 🔍 **Search & Filter** - ค้นหาและกรองสูตรอาหาร
- [ ] ❤️ **Favorites** - บันทึกสูตรโปรด  
- [ ] 📱 **Recipe Detail Screen** - หน้ารายละเอียดสูตร
- [ ] 🛒 **Shopping List** - รายการซื้อของ
- [ ] 👨‍🍳 **User Recipes** - อัพโหลดสูตรของตัวเอง
- [ ] 🌙 **Dark Mode** - โหมดมืด
- [ ] 📡 **Offline Support** - ใช้งานแบบออฟไลน์
- [ ] 🔔 **Push Notifications** - แจ้งเตือนสูตรใหม่

### 🔧 **Technical Improvements** 
- [ ] State Management (Provider/Riverpod/Bloc)
- [ ] Local Database (SQLite/Hive)
- [ ] Unit & Widget Testing
- [ ] CI/CD Pipeline
- [ ] Performance Optimization

---

## 📜 License

```
MIT License

Copyright (c) 2024 Delicious Recipes App

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 🤝 Contributing

เรายินดีต้อนรับการมีส่วนร่วมจากนักพัฒนาทุกคน!

### 📋 **How to Contribute**
1. Fork the project
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)  
5. Open a Pull Request

### 🌟 **Contributors**
- **[Your Name]** - *Initial work* - [GitHub Profile]

---

## 📞 Support & Contact

### 💬 **Get Help**
- 📧 Email: support@deliciousrecipes.app
- 💻 GitHub Issues: [Report Bug](../../issues)
- 📱 Discord: [Join Community](https://discord.gg/recipes)

### 🌟 **Show Your Support** 
ถ้าแอปนี้มีประโยชน์ กรุณา ⭐ Star repository นี้เพื่อเป็นกำลังใจ!

---

<div align="center">

**Made with ❤️ and Flutter**

*Happy Cooking! 👨‍🍳👩‍🍳*

[![Flutter](https://img.shields.io/badge/Built%20with-Flutter-blue?style=flat-square&logo=flutter)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Language-Dart-blue?style=flat-square&logo=dart)](https://dart.dev)

</div>
