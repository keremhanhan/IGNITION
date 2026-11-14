# IGNITION

**Different by Design.**

IGNITION is a 5v5 tactical first-person shooter in pre-production, developed by **Verse Mate Studios**.

The project is being designed around readable competitive gameplay, distinct operators, original weapons, and a structured round-based objective mode. This repository is intended to hold the project's development materials and, as implementation begins, its source code and supporting assets.

> **Project status:** Pre-production  
> **Design document:** GDD v0.2  
> **Target platform:** PC  
> **Engine:** Unreal Engine 5.7  
> **Primary language:** C++

---

## Overview

IGNITION is built around two opposing teams:

- **Attackers** aim to place the **Tek**.
- **Defenders** aim to prevent the placement or disable the Tek after it has been placed.
- Each team has **5 players**, for **10 players per match**.

The goal is to create a competitive tactical shooter with its own identity. Existing games may be used as broad design references, but IGNITION's names, models, sounds, animations, maps, and visual direction are intended to be original.

## Current Design

The following points reflect decisions recorded in GDD v0.2. They are design targets, not a claim that these systems have already been implemented.

### Game modes

- Derecesiz
- Rekabetçi
- Fast Verse

### Match structure

- 5v5 matches.
- Teams switch sides after the completion of round 12.
- The first team to win 13 rounds wins the normal match.
- Overtime is played in two-round sets. Teams switch sides after each set, and a team must lead by two rounds to win.

### Operator system

Each operator is planned to have four abilities, assigned to **Q, E, C, and X**. Operator identities, abilities, and balancing are still to be designed.

### Economy

| Item | Current design value |
|---|---:|
| Starting credits | 800 IC |
| Round win reward | 3,000 IC |
| First consecutive loss reward | 1,900 IC |
| Second consecutive loss reward | 2,400 IC |
| Third and later consecutive loss reward | 2,900 IC |
| Enemy elimination reward | 200 IC |

Unused credits carry over between rounds. Players retain their credits when eliminated. Economy timing, limits, and some distribution rules remain undecided.

### Initial weapon concepts

| Weapon | Category | Current concept | Magazine | Reserve | Cost |
|---|---|---|---:|---:|---:|
| DASH (WPN-001) | Rifle | Balanced rifle; automatic and semi-automatic fire modes | 25 | 50 | 2,900 IC |
| reICON (WPN-002) | Pistol | Free starting pistol; semi-automatic and alternate burst fire | 15 | 30 | 0 IC |

The first release is currently targeted to include **24 weapons**. Only the two concepts above have been defined at this stage.

### Maps

- **MASH** is planned as the initial map.
- **Texfi** and **Splash** are additional map concepts for later development.

## Technology

The current technical direction is:

- **Unreal Engine 5.7**
- **C++** for core gameplay systems
- **Blueprint** for visual, editor, and supporting tasks
- **PC** as the target platform

Planned development tools include Visual Studio 2022 and Blender. The server architecture is not finalized; a dedicated-server approach is being evaluated.

## Repository Status

This project is in **pre-production**. The design document records decisions and open questions; it does not mean every listed feature is implemented or ready for release.

At this stage, the repository may contain planning documents and project materials. Build instructions, installation steps, and playable releases will be added when the corresponding implementation is available.

## Roadmap

The current high-level roadmap is:

1. Expand and maintain the game design document.
2. Finalize the visual identity and user interface direction.
3. Design operators and their abilities.
4. Define the weapon and equipment roster.
5. Develop the MASH map.
6. Decide the technical and server architecture.
7. Establish the Unreal Engine project and core character movement.
8. Implement weapons, operators, maps, lobby, VERSE ID, matchmaking, and game modes.
9. Test, balance, fix issues, and optimize performance.

The order and scope may change as development progresses.

## Open Design Questions

Several areas are intentionally unresolved, including:

- Detailed round-win conditions and round duration
- Overtime starting score and initial side arrangement
- Economy reward timing, credit cap, and purchase time
- The remaining 22 weapons and weapon balance values
- Operator identities, abilities, and balance
- Rank system
- Detailed map layouts
- Server architecture and anti-cheat approach
- Character and weapon customization
- VERSE ID format and rules

These should be treated as open design work, not existing features.

## Contributing

IGNITION is currently in pre-production. If you want to discuss an idea or propose a contribution, open an issue with:

- A clear description of the suggestion or problem
- The design area it affects
- Relevant examples or supporting information

Please avoid submitting copied game assets, third-party intellectual property, or unlicensed material. Contributions should be discussed before being treated as part of the official design.

## License and Usage

The repository's `LICENSE.txt` describes the current rights notice. Unless a separate license explicitly says otherwise, no permission is granted to copy, modify, redistribute, or commercially use the project's code, documentation, artwork, audio, names, or other materials.

## Credits

**IGNITION**  
Developed by **Verse Mate Studios**

*Different by Design.*

---

<!-- TÜRKÇE SÜRÜM -->

# IGNITION

**Tasarımda Farklı.**

IGNITION, **Verse Mate Studios** tarafından geliştirilen ve ön üretim aşamasında bulunan 5'e 5 taktiksel birinci şahıs nişancı oyunudur.

Proje; kolay okunabilir rekabetçi oynanış, birbirinden farklı operatörler, özgün silahlar ve turlar üzerine kurulu hedef tabanlı bir oyun modu etrafında tasarlanmaktadır. Bu depo, projenin geliştirme belgelerini ve uygulama aşaması başladıkça kaynak kodunu ve destekleyici varlıklarını barındırmak için kullanılacaktır.

> **Proje durumu:** Ön üretim  
> **Tasarım belgesi:** GDD v0.2  
> **Hedef platform:** PC  
> **Oyun motoru:** Unreal Engine 5.7  
> **Ana programlama dili:** C++

---

## Genel Bakış

IGNITION, karşı karşıya gelen iki takım üzerine kuruludur:

- **Saldıranlar**, **Tek**'i yerleştirmeyi hedefler.
- **Savunanlar**, Tek'in yerleştirilmesini engellemeyi veya yerleştirildikten sonra etkisiz hâle getirmeyi hedefler.
- Her takımda **5 oyuncu** bulunur. Bir maçta toplam **10 oyuncu** yer alır.

Amaç, kendine özgü kimliği olan rekabetçi bir taktiksel nişancı oyunu oluşturmaktır. Mevcut oyunlar genel tasarım referansı olarak incelenebilir; ancak IGNITION'ın isimlerinin, modellerinin, seslerinin, animasyonlarının, haritalarının ve görsel yönünün özgün olması hedeflenmektedir.

## Mevcut Tasarım

Aşağıdaki maddeler GDD v0.2'de kayıtlı kararları yansıtır. Bunlar tasarım hedefleridir; sistemlerin hâlihazırda uygulanmış olduğu anlamına gelmez.

### Oyun modları

- Derecesiz
- Rekabetçi
- Fast Verse

### Maç yapısı

- Maçlar 5'e 5 oynanır.
- 12. turun tamamlanmasının ardından takımlar taraf değiştirir.
- Normal maçı ilk 13 tur kazanan takım kazanır.
- Uzatmalar ikişer turluk setler hâlinde oynanır. Her setten sonra takımlar taraf değiştirir. Bir takımın kazanması için 2 turluk fark oluşturması gerekir.

### Operatör sistemi

Her operatörün **Q, E, C ve X** tuşlarına atanmış dört yeteneğe sahip olması planlanmaktadır. Operatörlerin kimlikleri, yetenekleri ve denge ayarları henüz tasarlanmamıştır.

### Ekonomi

| Öğe | Mevcut tasarım değeri |
|---|---:|
| Başlangıç kredisi | 800 IC |
| Tur kazanma ödülü | 3.000 IC |
| İlk ardışık mağlubiyet ödülü | 1.900 IC |
| İkinci ardışık mağlubiyet ödülü | 2.400 IC |
| Üçüncü ve sonraki ardışık mağlubiyet ödülü | 2.900 IC |
| Rakip eleme ödülü | 200 IC |

Harcanmayan krediler sonraki turlara aktarılır. Oyuncular elendiklerinde kredilerini korur. Ekonomi ödüllerinin zamanlaması, sınırlar ve bazı dağıtım kuralları henüz belirlenmemiştir.

### İlk silah tasarımları

| Silah | Kategori | Mevcut tasarım | Şarjör | Yedek | Fiyat |
|---|---|---|---:|---:|---:|
| DASH (WPN-001) | Tüfek | Dengeli tüfek; tam otomatik ve yarı otomatik atış kipleri | 25 | 50 | 2.900 IC |
| reICON (WPN-002) | Tabanca | Ücretsiz başlangıç tabancası; yarı otomatik ve alternatif seri atış | 15 | 30 | 0 IC |

İlk sürümde **24 silah** bulunması hedeflenmektedir. Bu aşamada yalnızca yukarıdaki iki silahın tasarım fikri tanımlanmıştır.

### Haritalar

- **MASH**, ilk harita olarak planlanmaktadır.
- **Texfi** ve **Splash**, sonraki geliştirme aşamaları için ek harita fikirleridir.

## Teknoloji

Mevcut teknik yönelim şöyledir:

- **Unreal Engine 5.7**
- Temel oynanış sistemleri için **C++**
- Görsel, düzenleyici ve destekleyici görevler için **Blueprint**
- Hedef platform olarak **PC**

Planlanan geliştirme araçları arasında Visual Studio 2022 ve Blender bulunmaktadır. Sunucu mimarisi henüz kesinleştirilmemiştir; özel sunucu (Dedicated Server) yaklaşımı değerlendirilmektedir.

## Depo Durumu

Proje şu anda **ön üretim** aşamasındadır. Tasarım belgesi, alınan kararları ve açık soruları kaydeder; listelenen her özelliğin uygulanmış veya yayıma hazır olduğu anlamına gelmez.

Bu aşamada depoda planlama belgeleri ve proje materyalleri bulunabilir. Derleme yönergeleri, kurulum adımları ve oynanabilir sürümler, ilgili uygulamalar hazır olduğunda eklenecektir.

## Yol Haritası

Mevcut üst düzey yol haritası şöyledir:

1. Oyun tasarım belgesini genişletmek ve güncel tutmak.
2. Görsel kimliği ve kullanıcı arayüzü yönünü kesinleştirmek.
3. Operatörleri ve yeteneklerini tasarlamak.
4. Silah ve ekipman listesini belirlemek.
5. MASH haritasını geliştirmek.
6. Teknik ve sunucu mimarisine karar vermek.
7. Unreal Engine projesini ve temel karakter hareketini oluşturmak.
8. Silahları, operatörleri, haritaları, lobiyi, VERSE ID'yi, eşleştirmeyi ve oyun modlarını uygulamak.
9. Test etmek, dengelemek, hataları düzeltmek ve performansı iyileştirmek.

Geliştirme ilerledikçe sıra ve kapsam değişebilir.

## Açık Tasarım Konuları

Bazı alanlar bilerek henüz karara bağlanmamıştır:

- Tur kazanma koşullarının ayrıntıları ve tur süresi
- Uzatmanın başlangıç skoru ve ilk taraf düzeni
- Ekonomi ödüllerinin zamanlaması, kredi üst sınırı ve satın alma süresi
- Kalan 22 silah ve silah denge değerleri
- Operatör kimlikleri, yetenekleri ve denge ayarları
- Rütbe sistemi
- Haritaların ayrıntılı yerleşimleri
- Sunucu mimarisi ve hile karşıtı yaklaşım
- Karakter ve silah özelleştirmeleri
- VERSE ID biçimi ve kuralları

Bunlar mevcut özellikler olarak değil, üzerinde çalışılması gereken tasarım konuları olarak değerlendirilmelidir.

## Katkıda Bulunma

IGNITION şu anda ön üretim aşamasındadır. Bir fikri tartışmak veya katkı önermek istiyorsan aşağıdaki bilgileri içeren bir konu (issue) aç:

- Önerinin veya sorunun açık bir açıklaması
- Etkilediği tasarım alanı
- İlgili örnekler veya destekleyici bilgiler

Kopyalanmış oyun varlıkları, üçüncü taraf fikrî mülkiyetleri veya lisanssız materyaller göndermekten kaçın. Katkılar, resmî tasarımın parçası olarak kabul edilmeden önce görüşülmelidir.

## Lisans ve Kullanım

Depodaki `LICENSE.txt` dosyası mevcut hak bildirimini açıklar. Ayrı bir lisans açıkça aksini belirtmediği sürece projenin kodunu, belgelerini, görsellerini, seslerini, isimlerini veya diğer materyallerini kopyalamak, değiştirmek, yeniden dağıtmak ya da ticari amaçla kullanmak için izin verilmemektedir.

## Emeği Geçenler

**IGNITION**  
Geliştiren: **Verse Mate Studios**

*Tasarımda Farklı.*
