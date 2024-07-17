### Turbo Native Module ve Fabric Native Components

React Native ekosisteminde yer alan iki önemli teknoloji olan Turbo Native Module ve Fabric Native Components, performans iyileştirmeleri ve daha iyi kullanıcı deneyimi sunmayı amaçlar. Bu teknolojiler, React Native'in gelecekteki sürümlerinde önemli rol oynayacak yeniliklerdir ve farklı işlevleri vardır.

#### Turbo Native Module
Turbo Native Module, React Native'de JavaScript ve yerel (native) kod arasındaki iletişimi daha hızlı ve verimli hale getirmek için geliştirilmiştir.

**Ana Özellikleri:**
1. **JIT ve AOT Yürütme**: Just-In-Time (JIT) ve Ahead-Of-Time (AOT) yürütme yöntemlerini kullanarak daha hızlı ve optimize edilmiş kod çalıştırma sağlar.
2. **Senkron ve Asenkron İletişim**: JavaScript ile yerel kod arasında daha verimli bir şekilde senkron ve asenkron iletişim kurmayı mümkün kılar.
3. **Daha Az Geçiş**: JavaScript ile yerel kod arasında daha az geçiş (bridge) yaparak performansı artırır ve gecikmeleri azaltır.
4. **Kod Boyutu ve Bellek Kullanımı**: Bellek kullanımı ve kod boyutunu optimize ederek daha hafif ve performanslı uygulamalar geliştirmeyi sağlar.

**Örnek:**
```typescript
// Turbo Native Module Kullanımı (temsilî kod)
function add(a: number, b: number): number {
    return a + b;
}
```

#### Fabric Native Components
Fabric Native Components, React Native'in yeni bir mimarisidir ve mevcut UIManager'ın yerini alarak daha hızlı ve verimli bir kullanıcı arayüzü (UI) oluşturmayı hedefler.

**Ana Özellikleri:**
1. **Senkron ve Asenkron Rendering**: Senkron ve asenkron rendering yetenekleri sunarak daha esnek ve performanslı bir UI oluşturma imkanı sağlar.
2. **Modernizasyon**: React Fiber ile uyumlu olacak şekilde modernize edilmiştir ve mevcut mimariye kıyasla daha hızlı UI güncellemeleri sunar.
3. **Doğrudan Shadow Tree Manipülasyonu**: Shadow tree'yi doğrudan manipüle edebilir, bu da daha hızlı UI güncellemeleri ve daha az bridge geçişi sağlar.
4. **Zamanlama ve Performans İyileştirmeleri**: UI güncellemelerinin zamanlamasını ve performansını optimize eder, daha hızlı ve sorunsuz bir kullanıcı deneyimi sağlar.

**Örnek:**
```typescript
// Fabric Native Components Kullanımı (temsilî kod)
const MyComponent = () => {
    return (
        <View>
            <Text>Hello, Fabric!</Text>
        </View>
    );
};
```

### Özet
- **Turbo Native Module**: JavaScript ve yerel kod arasındaki iletişimi hızlandırmayı ve optimize etmeyi amaçlayan bir teknoloji. Özellikleri arasında daha hızlı JIT/AOT yürütme, senkron ve asenkron iletişim, daha az bridge geçişi bulunur.
- **Fabric Native Components**: React Native'in UI oluşturma mimarisini yenileyen bir teknoloji. Senkron ve asenkron rendering, doğrudan shadow tree manipülasyonu, modernizasyon ve performans iyileştirmeleri gibi özellikler sunar.

Her iki teknoloji de React Native uygulamalarında performans ve kullanıcı deneyimini iyileştirmeyi hedefler, ancak farklı alanlarda çalışırlar: Turbo Native Module, JavaScript-yerel kod iletişimini, Fabric Native Components ise komponent rendering sürecini optimize eder.