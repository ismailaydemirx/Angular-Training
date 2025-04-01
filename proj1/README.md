### **Angular Nedir?**

Angular, Google tarafından geliştirilen modern web uygulamaları oluşturmak için kullanılan bir front-end framework'üdür. Özellikle:

- **Component tabanlı mimari** sayesinde uygulamaları modüler parçalara böler
- **TypeScript** desteği ile daha güvenli ve okunabilir kod yazmayı sağlar
- **Two-way data binding** özelliği ile veri ve arayüz senkronizasyonunu otomatikleştirir
- **Dependency injection** sistemiyle bileşenler arası bağımlılıkları yönetir

**Örnek Kullanım:**

```tsx
@Component({
  selector: 'app-greeting',
  template: `<h1>Merhaba {{userName}}!</h1>`
})
export class GreetingComponent {
  userName = 'Ahmet';
}
```

**Kaynak:** [Angular Resmi Dokümantasyonu](https://angular.io/docs)

---

### **SPA (Single Page Application) Nedir?**

SPA'lar tek bir HTML sayfası üzerinde çalışan ve içeriği dinamik olarak değiştiren uygulamalardır:

**Avantajları:**

- Daha hızlı kullanıcı deneyimi
- Sunucuya daha az istek
- Mobil uygulama benzeri akıcılık

**Angular'da SPA:**

- Router modülü sayesinde farklı görünümler arasında geçiş yapılabilir
- Lazy loading ile performans optimize edilebilir

**Kaynak:** [MDN SPA Tanımı](https://developer.mozilla.org/en-US/docs/Glossary/SPA)

---

### **Angular Geliştirme Ortamı Kurulumu**

Angular'da geliştirme yapmak için gerekenler:

1. **Node.js (v14+)** - JavaScript runtime ortamı
2. **npm/yarn** - Paket yöneticisi
3. **Angular CLI** - Komut satırı arayüzü, bu asistan üzerinden Angular uygulamaları oluşturmaktan tutun, Angular’ın temel yapı taşlarını üretebilecek ve hızlıca geliştirmemize odaklanabileceğiz. (Node.js gereklidir.)
4. **IDE (VS Code önerilir)** - Kod editörü

**Kontrol Komutları:**

```bash
node -v  # Node.js versiyon kontrolü
npm -v   # npm versiyon kontrolü
```

---

### **Angular CLI Kurulumu ve Kullanımı**

Angular CLI, proje oluşturma ve yönetme işlemlerini kolaylaştırır:

**Kurulum:**

```bash
npm install -g @angular/cli
```

-g parametresi bu talimatın ilgili bilgisayar için global olduğunu ifade etmektedi. Yani talimat neticesinde kurulacak Angular CLI’ın sadece ilgili path üzerinde değil tüm pc üzerinde erişilebilir ve kullanılabilir olduğunu ifade etmektedir.

Bu talimat neivesinde bilgisayarınıza Angular CLI’ı kurmuş olacaksınız.

Test etmek için CMD üzerinden **ng —help** komutunu çalıştırabiliriz.

**Temel Komutlar:**

```bash
ng version: kullanılan angular versiyon bilgisini verir.
ng new proje-adi      # Yeni proje oluşturma
ng serve --open      # Development sunucusunu başlatma (uygulamayı ayağa kaldırma)
ng generate component component-adi  # Yeni component oluşturma
```

**Kaynak:** [Angular CLI Dokümantasyonu](https://angular.io/cli)

---

### **Angular'da Kullanılan Dil: TypeScript**

Angular uygulamaları Javascript’in bir konsepti olan **TypeScript** ile yazılır:

**TypeScript Avantajları:**

- Statik tip kontrolü
- Sınıf tabanlı programlama
- Daha iyi IDE desteği
- JavaScript'in tüm özelliklerini içerir
- Javascript’i OOP nimetlerinden faydalanarak daha okunaklı ve anlaşılır bi şekilde geliştirmemizi sağlayan, derlendiği takdirde JavaScript çıktısı veren bir konseptir diyebiliriz.

**Örnek TypeScript Kodu:**

```tsx
interface User {
  name: string;
  age: number;
}

const user: User = { name: "Ayşe", age: 30 };
```

---

### **Angular Proje Yapısı**

Tipik bir Angular projesinin temel dizin yapısı:

```
src/
├── app/
│   ├── app.component.ts    # Ana component
│   ├── app.module.ts       # Ana modül
│   └── ...                 # Diğer componentler
├── assets/                 # Statik dosyalar
├── index.html              # Ana HTML dosyası
└── main.ts                 # Uygulama giriş noktası
```
 
**Önemli Dosyalar:**

- `angular.json`: Proje konfigürasyonu
- `package.json`: Bağımlılıklar
- `tsconfig.json`: TypeScript ayarları
- **node_modules:**  Uygulamada kullanılan paketler bu dizinde  bulunur.

![image](https://github.com/user-attachments/assets/6534755e-94bb-412c-a6ee-b855bb98b1e1)


- `src`  (Source) klasörünün içindeki `app` klasörü, genellikle bir Angular projesinin ana klasör yapısında yer alır. Uygulamanın en önemli klasörüdür. Uygulamayla ilgili hayati dosyalar bu klasörde bulunur. Çalışmalarımızın büyük kısmı (%99’u) bu klasörde gerçekleşecektir.
- `app` klasörü, Angular uygulamasının **temel bileşenlerini içerir.** Bu bileşenler genellikle **modüller**, **bileşenler**, **servisler**, **yönlendirme ayarları** gibi kod parçalarını içerir.
- Proje uygulamasının merkezi olan `app` klasörü, Angular tarafından **başlatılan ve yürütülen ana uygulamayı** temsil eder.
- **assests:** Uygulamayla ilgili resim, icon, video vs. dosyaları bu klasörde bulunur.
- **index.html:** Temel geliştirme sayfasıdır. İçinde uygulamanın temel direktifini barındırmaktadır.
- **main.ts:** Uygulamanın giriş/başlangıç dosyasıdır. C#’daki ‘Program.cs’ dosyasına muadildir diyebiliriz. Uygulama sürecinde hangi modülün ana modül olacağı burada belirtilmektedir.

- **.editorconfig:** Editörle ilgili temel konfigürasyonlar bu dosyada gerçekleştirilir.
- **angular.json:** Uygulamayla ilgili script, style, budgets vs. gibi temel kofigürasyonların yapıldığı dosyadır.
- **package-lock.json:** Uygulamada kullanılan paketlerin sürümleri hakkında bilgi içerir. Böylece uygulama sürecinde paketlerin sürümleri ve bağımlılıklarını doğru şekilde yönetmek için kullanılmaktadır.
- **tsconfig.json:** TypeScript ile ilgili konfigürasyonların bulunduğu klasördür.
- **package-json:** Uygulamada kullanılan paketlerin listesini tutmaktadır.
- Bu klasörde genellikle "**app.module.ts**" gibi ana modül dosyası, kullanılacak bileşenlerin ve hizmetlerin tanımlandığı birimler bulunur.
- Ayrıca, proje içerisindeki farklı sayfalar veya özellikler için ayrı alt klasörler de oluşturulabilir, bu alt klasörlerde ilgili bileşen dosyaları ve hizmet dosyaları yer alabilir.

![image](https://github.com/user-attachments/assets/16b491a1-002b-43c0-9dbb-9add60183818)


Yukarıda, **angular.json** içinde bulunan **styles**  kısmını css kısımları için **scripts** kısmını ise script dosyaları için projeden herhangi bir şekilde izin almadan yükleyebileceğimiz kısımlardır.

---

![image](https://github.com/user-attachments/assets/cfde78cb-7c67-44ba-ba66-1cdf121a101b)


- **Components**, Angular projelerinde web sayfalarındaki farklı bölümleri temsil eder ve **iletişim kurabilirler**.
- Varsayılan olarak "**App**" componenti gelir ve yapısı belirli dosyalarla tanımlanır.
- Yeni bir component oluşturmak için terminalde belirli komutlar kullanılır.
- Components içinde değişkenler ve fonksiyonlar tanımlanabilir ve bunlar, component açıldığında çalışacak şekilde ayarlanabilir.
- Kısaca **her şeyi bir component** olarak oluşturabilir ve bu component’ler arasında **iletişimi** sağlayabiliriz.

### app.component.ts

```csharp
import { Component } from '@angular/core';
import { RouterOutlet } from '@angular/router'; // RouterOutlet'ı Angular'ın router'ından alıyoruz.

@Component({
  selector: 'app-root', // Bu component'i çağırmak istediğimizde kullanacağımız ad
  standalone: true, // Bu bileşenin kendi başına çalışabilir olduğunu belirtir.
  imports: [RouterOutlet], // Bu bileşenin RouterOutlet'ı içe aktardığını belirtir, ancak RouterOutlet bileşeni normalde dış modülden alınmaz.
  templateUrl: './app.component.html', // Bu template'in görünümünü hangi HTML'den alacağını gösterir.
  styleUrl: './app.component.scss' // Bu bileşenin stillerini gösterir, SCSS dosyasının yolu.
})
export class AppComponent { // Class içerisinde değişkenlerimizi ve metodlarımızı tanımlayabiliriz.
  title = 'OrnekProje'; // Bileşenin veri bağlamı, "OrnekProje" başlığını içerir.
}

```

---

**Şimdi biz yeni bir component oluşturalım.**

Terminal’e geliyoruz, projemizin içindeki dizindeyken

```csharp
ng g component [**componentAdi**]

buradaki g= generate'nin g'si

kısaca

ng g c [componentAdi]

şeklinde de yapabiliriz.
```

Mesela biz header component’i oluşturalım

```csharp
ng g component components/header

yukarıda **components klasörü** içerisinde header adında component oluşturduk.
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/dac8fad1-6570-4416-bf03-d9507a444681/70e40525-aff5-42d2-b021-3d202582727a/Untitled.png)

src → app → components → header adında 1 component oluşturduk.

---

### Routing:

Şimdi routing ile kullanıcının view’lar arasında dolaşmasını sağlayalım.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/dac8fad1-6570-4416-bf03-d9507a444681/ba635dd2-4b27-431b-b5c3-caa8129d5cc5/Untitled.png)

**app→ app.routes.ts**

yukarıdaki ts dosyasında 

```csharp
export const routes: Routes = [];
```

kısmını kullanarak routing yapacağız.

---

Şimdi aşağıda routing kısmında component’lerimiz için tanımlarımızı yaptık.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/dac8fad1-6570-4416-bf03-d9507a444681/0d9e24f3-2483-457b-8eb8-57041e6e66c1/Untitled.png)

Tanımları yaptıktan sonra [localhost:4200/about](http://localhost:4200/about) veya [localhost:4200/](http://localhost:4200/about)contact sitelerine gittiğimizde herhangi bir şey gözükmezse bu **app.component.html** dosyasında **router-outlet** taglarını açmadığımızdan kaynaklıdır.

Aşağıdaki gibi tanım yapmalıyız.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/dac8fad1-6570-4416-bf03-d9507a444681/b2549173-0a05-40df-b3d2-9fa19e0b4bd1/Untitled.png)

---

### **Angular Uygulamasını Çalıştırma**

Uygulamayı başlatmak için:

```bash
ng serve
```

Bu komut:

- Uygulamayı derler
- Localhost:4200'de bir sunucu başlatır
- Değişiklikleri otomatik olarak yeniler (hot reload)

**Production Build:**

```bash
ng build --prod

```

---

### **Angular Language Service**

VS Code için Angular Language Service eklentisi:

**Özellikleri:**

- Otomatik tamamlama
- Hata denetimi
- Kod navigasyonu
- Refactoring desteği

**Kurulum:**

1. VS Code'da Angular Language Service eklentisini yükleyin
2. Projeye dependency ekleyin:

```bash
npm install @angular/language-service --save-dev

```

**Kaynak:** [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
