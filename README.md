# Taiko Node Test Kurulum Rehberi

![Taiko-Node-Testi](https://mirror-media.imgix.net/publication-images/4qVW-dWhNmMQr61g91hGt.png?height=512&width=1024&h=512&w=1024&auto=compress)


### Önerilen Sistem Gereksinimleri;

|CPU | RAM  | Disk  | 
|----|------|----------|
|  2| 6GB  | 50GB    |

 # Daha önce Node kurulumu yapmadıysanız buradan sırasıyla adımları takip ederek tüm süreci öğrenebilirsiniz.
  ## Yeni Başladım Rehberi; <a href="https://coinhunterstr.com/category/testnet/" target="_blank"> Coin Hunters </a>
  ### 1. [Testnet ve Node test kurulum rehberi Bölüm-1](https://coinhunterstr.com/testnet-ve-node-kurulum-rehberi/)
  ### 2. [Yeni Chrome Tarayıcı nasıl açarım?](https://coinhunterstr.com/yeni-chrome-tarayici-nasil-acarim/)
  ### 3. [Ücretsiz Sunucu Kiralama](https://coinhunterstr.com/ucretsiz-sunucu-nasil-kiralarim/)
  ### 4. [Digital Ocean Nasıl Kayıt olurum?](https://coinhunterstr.com/digital-oceana-nasil-kayit-olabilirim/)
  ### 5. [MobaXTerm Terminal Kurulumu](https://coinhunterstr.com/mobaxterm-terminal-kurulumu/)
  
## UYARI

Taiko Node testneti ETH üzerinde ZKP ve gizlilik odaklı bir L2 çözümü, ödül ve yatırımcılar konusunda henüz bir açıklama yok. Bu nedenle kurup kurmamak size kalmış. Biz kurduğumuz için rehberini yayınlıyoruz.


## Kurulum:
* Komutları tek tek girin.

```
sudo apt update 
```
```
sudo apt upgrade
```
```
apt install docker-compose
```
```
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin
```

## Repoyu Klonluyoruz.
```
git clone https://github.com/taikoxyz/simple-taiko-node.git
cd simple-taiko-node
```
## Ayrı screende çalıştıracağız:
```
screen -S taiko
```

## İçine girip düzenlemeler yapıyoruz:
```
cp .env.sample .env
nano .env
```
## Bu kısıma devam etmeden önce sıfırdan metamask oluşturup token alıyoruz, veya testnetler için kullandığın metamaskı'ın private key anahtarı gerekiyor.
### Metamask Private Key alma;
> Metamask cüzdanımızı oluşturduktan sonra; Aşağıdaki görseldeki adımları takip ederek private key'inizi alabilirsiniz.
![matemask-private-key](https://user-images.githubusercontent.com/111747226/214060644-f8045d6d-2bd7-47de-80ee-046e859fe9fe.png)


## Yukarıdaki komutları girince açılacak ekran görselde ki gibi.

* Açıldıktan sonra yön tuşları ile en alta geliyoruz.
* `ENABLE_PROPOSER` kısmını `true` yapıyoruz
* `L1_PROPOSER_PRIVATE_KEY=` kısmına metamasktan private key alıyoruz (2. görsele bakın)
* `L2_SUGGESTED_FEE_RECIPIENT=`bu kısımda `Metamask 0x Cüzdan Adresi` olacak
* sonra CTRL + X + Y ile çıkıyoruz.

![image](https://user-images.githubusercontent.com/76253089/212540636-32564971-d531-41f2-b2a6-ffc5ef21582c.png)

* Metamasktan 3 noktaya tıklayınca hesap bilgileri kısmında olacak burası:
![image](https://user-images.githubusercontent.com/101149671/212497188-e5480587-9872-4c0f-abf0-4f6b24839396.png)

## Node'u çalıştırın:
```
docker compose up -d
```
## Node'unuz çalışıyor kolay gelsin:

![image](https://user-images.githubusercontent.com/101149671/212497350-4cebdcc6-edeb-4949-b18b-a38a83e1a53c.png)

## Taiko yatırımını açıklamamış projelerden birisidir.







## Iron Fish Discord kanalına katılmayı unutmayın;
### [Discord](https://discord.gg/35ZxaUquTc)

## Yarım için telegram kanalımız;
### [Coin Hunters Telegram](https://t.me/CoinHuntersTR)
