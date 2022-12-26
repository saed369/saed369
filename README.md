- 👋 Hi, I’m @saed369
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
saed369/saed369 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>
#include <string>

using namespace std;

int main() {
  int count = 0;  // متغير لحساب عدد الاحتمالات

  // البدء من aa00 إلى zz99
  for (char c1 = 'a'; c1 <= 'z'; c1++) {
    for (char c2 = 'a'; c2 <= 'z'; c2++) {
      for (int i = 0; i <= 99; i++) {
        string password = string(1, c1) + string(1, c2) + to_string(i);
        while (password.length() < 5) {  // ملء الخانات الفارغة بـ 0
          password = "0" + password;
        }
        cout << password << endl;  // طباعة كلمة السر
        count++;  // تعديل العدد الحالي للاحتمالات
      }
    }
  }

  cout << "Number of possibilities: " << count << endl;  // طباعة العدد الإجمالي للاحتمالات

  return 0;
}
