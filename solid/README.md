## SOLID

1.  Single Responsibility Principle (SRP)

Không được có nhiều lý do để thay đổi class. Cần hạn chế số lần thay đổi class. Bởi vì khi cần thay đổi 1 function trong class thì rất khó để kiếm tra ảnh hưởng của nó lên các function khác.

**Bad**
```javascript
class UserSettings {
  constructor(user) {
    this.user = user;
  }

  changeSettings(settings) {
    if (this.verifyCredentials()) {
      // ...
    }
  }

  verifyCredentials() {
    // ...
  }
