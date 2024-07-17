SOLID prensipleri, yazılım geliştirmede daha esnek, yeniden kullanılabilir ve sürdürülebilir kod yazmak için kullanılan beş temel prensiptir:

### 1. **Single Responsibility Principle (SRP)**

Her sınıfın veya fonksiyonun yalnızca bir sorumluluğu olmalıdır.

#### Örnek:

```jsx
// Kötü örnek
function UserComponent() {
  // Kullanıcı bilgilerini çekme
  const fetchUser = () => {
    /* ... */
  };
  // Kullanıcı arayüzünü oluşturma
  return <div>{/* ... */}</div>;
}

// İyi örnek
function UserComponent({ user }) {
  return <div>{/* ... */}</div>;
}

function fetchUser() {
  // Kullanıcı bilgilerini çekme
}
```

### 2. **Open/Closed Principle (OCP)**

Yazılım varlıkları genişletmeye açık olmalı, ancak değişikliğe kapalı olmalıdır.

#### Örnek:

```jsx
// Kötü örnek
function renderShape(shape) {
  if (shape.type === 'circle') {
    // çember çiz
  } else if (shape.type === 'square') {
    // kare çiz
  }
}

// İyi örnek
class Shape {
  draw() {}
}

class Circle extends Shape {
  draw() {
    /* çember çiz */
  }
}

class Square extends Shape {
  draw() {
    /* kare çiz */
  }
}
```

### 3. **Liskov Substitution Principle (LSP)**

Bir sınıfın alt sınıfları, türetildikleri sınıfın yerine kullanılabilmelidir.

#### Örnek:

```jsx
// Kötü örnek
class Bird {
  fly() {
    /* uçar */
  }
}

class Penguin extends Bird {
  fly() {
    throw new Error("Penguins can't fly!");
  }
}

// İyi örnek
class Bird {
  move() {
    /* hareket eder */
  }
}

class Penguin extends Bird {
  move() {
    /* yürür */
  }
}
```

### 4. **Interface Segregation Principle (ISP)**

Kullanıcıların ihtiyaç duymadıkları işlevleri içeren arayüzlere bağımlı olmaları zorlanmamalıdır.

#### Örnek:

```jsx
// Kötü örnek
class LargeInterface {
  method1() {
    /* ... */
  }
  method2() {
    /* ... */
  }
}

class Implementation implements LargeInterface {
  method1() {
    /* ... */
  }
  method2() {
    /* ... */
  }
}

// İyi örnek
class Interface1 {
  method1() {
    /* ... */
  }
}

class Interface2 {
  method2() {
    /* ... */
  }
}

class Implementation implements Interface1, Interface2 {
  method1() {
    /* ... */
  }
  method2() {
    /* ... */
  }
}
```

### 5. **Dependency Inversion Principle (DIP)**

Üst seviye modüller alt seviye modüllere bağımlı olmamalıdır. Her ikisi de soyutlamalara bağımlı olmalıdır.

#### Örnek:

```jsx
// Kötü örnek
class User {
  constructor() {
    this.logger = new ConsoleLogger();
  }
}

// İyi örnek
class User {
  constructor(logger) {
    this.logger = logger;
  }
}

class ConsoleLogger {
  log(message) {
    /* ... */
  }
}

// Kullanım
const logger = new ConsoleLogger();
const user = new User(logger);
```

Bu prensipler, React ve React Native projelerinde daha modüler, test edilebilir ve sürdürülebilir kod yazmayı sağlar.
