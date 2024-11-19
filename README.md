<div align="center">
  <br />
  <p>
    <a href="https://discord.js.org"><img src="https://discord.js.org/static/logo.svg" width="546" alt="discord.js" /></a>
  </p>
</div>

# FindCord API

FindCord API, kullanıcılara çeşitli bilgilere erişim sağlayan bir API'dir. API, farklı endpointler aracılığıyla veriler sunar ve çeşitli hizmetler sağlar.

## API Hakkında

- FindCord API, kullanıcıların günlük hayatlarında ihtiyaç duydukları çeşitli bilgilere erişim sağlar. Hava durumu, burç bilgisi, döviz kuru, namaz vakitleri gibi çeşitli hizmetler sunar.
- FindCord'nin en önemli özelliği ise discord kullanıcılarını stalklamak.

## Kullanım

API'yi kullanmak için çeşitli endpointler bulunmaktadır. İşte bazı örnek endpointler:

- `/user/{id}` - Kullanıcı Bilgisi
- `/burc/{isim}` - Burç Bilgisi
- `/gunlukburc/{isim}` - Günlük Burç Bilgisi
- `/haftalikburc/{isim}` - Haftalık Burç Bilgisi
- `/aylikburc/{isim}` - Aylık Burç Bilgisi
- `/weather/{isim}/` - Hava Durumu Bilgisi
- `/iltifat` - İltifat
- `/doviz` - Döviz Kuru Bilgisi
- `/namaz/{sehir}/{ilce}` - Namaz Vakitleri
- `/nsfw` - NSFW İçerik //

Daha fazla endpoint ve kullanım bilgisi için [API Dökümantasyonu](https://api.findcord.com/document) sayfasını ziyaret edebilirsiniz.

## Npm Paketiyle Veri Çekmek Icin
- https://www.npmjs.com/package/mys-api.js

## Veri Çekme Örneği

Aşağıdaki örnek kod, Axios kullanarak bir API'den veri çekmek için kullanılabilir. API anahtarınızı ve API URL'sini kod içinde belirtmelisiniz.

```javascript
const axios = require('axios');

async function fetchData() {
    const apiUrl = `https://api.findcord.com/api/user/{id}`; // İstek atılacak API URL'sini belirtin
    
    try {
        const response = await axios.get(apiUrl);
        
        console.log("İstek Başarılı!", response.data);

    } catch (error) {
        console.error('Hata:', error);
    }
}

fetchData();
```

## Örnek Ekran Görüntüleri
![Örnek Ekran Görüntüsü](https://github.com/user-attachments/assets/749ebe5f-efa5-475f-a123-c536bba2ff01)

![Örnek Ekran Görüntüsü 2](https://github.com/user-attachments/assets/0cc75585-ec71-4603-a8c7-11f305ab646b)


## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasını inceleyebilirsiniz.
