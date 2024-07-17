## TypeScript: Interface ve Type Arasındaki Fark

TypeScript'te `interface` ve `type`, nesne şekillerini tanımlamak için kullanılır. Aralarındaki farklar ve kullanım alanları:

### Interface:

- **Genişletilebilir ve Birleştirilebilir:** Bir `interface` birden fazla tanımda birleştirilebilir ve genişletilebilir.
- **Sınıf Uygulamaları:** Sınıflar için şablon oluşturmak amacıyla kullanılır.

### Type:

- **Daha Esnek:** Union, intersection gibi daha karmaşık tip tanımlamaları yapabilir.
- **Takma Adlar:** Mevcut türler için takma adlar (alias) oluşturmak için kullanılır.

#### Örnekler:

```typescript
// Interface Örneği
interface Person {
  name: string;
  age: number;
}

interface Employee extends Person {
  employeeId: number;
}

interface Person {
  gender: string; // Birleştirilebilir ve genişletilebilir
}

// Type Örneği
type ID = number | string;

type Point = {
  x: number;
  y: number;
};

type ColorPoint = Point & {
  color: string;
};
```
