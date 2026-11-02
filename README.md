# turkpin-api-v1-client-packages

Turkpin bayi API'si (v1) için farklı dillerde yazılmış istemci paketleri. Her paket kendi deposunda geliştirilir; bu depo hepsini git submodule olarak bir arada tutar.

> Paketler topluluk tarafından yazılmıştır; Turkpin'in resmi paketleri değildir. API'nin güncel ve bağlayıcı tanımı için [dev.turkpin.com](https://dev.turkpin.com) dokümanına bakın.

| Dil | Klasör | Depo | Framework entegrasyonu |
|---|---|---|---|
| PHP 8.1+ | [`turkpin-php`](turkpin-php) | [buluterol/turkpin-php](https://github.com/buluterol/turkpin-php) | Laravel, Symfony |
| Node.js 18+ | [`turkpin-node`](turkpin-node) | [buluterol/turkpin-node](https://github.com/buluterol/turkpin-node) | NestJS (Express, Fastify, Next.js örnekleri) |
| Python 3.8+ | [`turkpin-python`](turkpin-python) | [buluterol/turkpin-python](https://github.com/buluterol/turkpin-python) | Django, Flask, FastAPI |
| Go 1.21+ | [`turkpin-go`](turkpin-go) | [buluterol/turkpin-go](https://github.com/buluterol/turkpin-go) | net/http, Gin, Echo, Fiber örnekleri |
| Java 11+ | [`turkpin-java`](turkpin-java) | [buluterol/turkpin-java](https://github.com/buluterol/turkpin-java) | Spring Boot 2.7 / 3.x |
| .NET Standard 2.0 | [`turkpin-dotnet`](turkpin-dotnet) | [buluterol/turkpin-dotnet](https://github.com/buluterol/turkpin-dotnet) | ASP.NET Core (DI) |
| Ruby 2.6+ | [`turkpin-ruby`](turkpin-ruby) | [buluterol/turkpin-ruby](https://github.com/buluterol/turkpin-ruby) | Rails |
| Rust | [`turkpin-rust`](turkpin-rust) | [buluterol/turkpin-rust](https://github.com/buluterol/turkpin-rust) | Axum, Actix Web örnekleri |

Tüm paketler aynı API komutlarını kapsar: `epinOyunListesi`, `epinUrunleri`, `epinSiparisYarat` (ön sipariş ve barem dahil), `siparisDurumu`, `siparisListesi`, `balance`. Kurulum ve kullanım her paketin README dosyasındadır.

## İndirme

```sh
git clone --recurse-submodules https://github.com/buluterol/turkpin-api-v1-client-packages.git
```

Daha önce submodule'ler olmadan klonladıysanız:

```sh
git submodule update --init
```

Paketleri en son sürümlerine çekmek için:

```sh
git submodule update --remote
```

## Test ortamı

- Test: `https://www.turkpin.net/api.php`, canlı: `https://www.turkpin.com/api.php`.
- Test ortamına erişmek için sunucu IP adresinizin Turkpin'e tanıtılması gerekir; tanıtılmamış IP'den gelen isteklere API `002` hata koduyla cevap verir.
- Kullanıcı adı ve şifreyi koda yazmayın; ortam değişkeni ya da gizli anahtar deposundan okuyun.

## English

Client packages for the Turkpin dealer API v1 in PHP, Node.js, Python, Go, Java, .NET, Ruby and Rust, collected here as git submodules (each package lives in its own repository). Community-maintained, not official Turkpin packages; see [dev.turkpin.com](https://dev.turkpin.com) for the authoritative API reference. Clone with `git clone --recurse-submodules`.

## Lisans

MIT. Her paketin kendi LICENSE dosyası vardır.
