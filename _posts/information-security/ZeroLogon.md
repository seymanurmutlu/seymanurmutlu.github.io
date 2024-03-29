---
layout: post
title:  "Zero Logon Zafiyeti"
date:   2022-11-29 14:46:09 +0300
categories: information-security
---
Keywords:
Lateral Movement
MS-NRPC(Netlogon Remote Protocol) 
CVE-2020-1472 
# Zerologon Nedir?
Windows Server ve Active Directory’deki MS-NRPC(Netlogon Remote Protocol) protokolünü hedef alan zafiyet, kötü amaçlı saldırganın hiçbir kimliğe ya da yetkiye sahip olmadan sadece ağda bir TCP bağlantısına sahip olmasıyla bütün Domain Controller yetkilerini eline geçirmesine sebep oluyor.

Zafiyet, MS-NRPC’de bulunan ComputeNetlogonCredential fonksiyonundaki AES-CFB8 şifrelemesinin ve oturum anahtarı için anahtar türetme fonksiyonunun (KeyDerivationFunction) yanlış yapılandırılmasından dolayı ortaya çıkıyor. Bu yapılandırılmanın sömürülmesi, MS-NRPC’nin yetkilendirme protokolünde oluşturduğu oturum anahtarını 0 değerleri ile oluşturmasıyla saldırganın Domain Controller’ın parolasını sıfırlamasına sebep oluyor. Bu nedenle zafiyetin ismi “Zerologon” olarak adlandırılıyor.

Zerologon güvenlik açığı, rastgele oluşturulan her 256 anahtardan 1’i için null baytlardan oluşan bir düz metnin (plain text) şifrelenmesi sonucunda, null baytlardan oluşan bir şifreli (cipher text) metnin oluşmasına neden olan kriptografik hatadan kaynaklanıyor. Zafiyetli şifreleme protokolü, netlogon protokolündeki kimlik doğrulama mekanizması yerine uygulanır.

# Etkilenen Sistemler 
Windows Server 2019 ve Windows Server 2016’nın herhangi bir sürümünün yanı sıra Windows Server sürüm 1909, Windows Server sürüm 1903, Windows Server sürüm 1809 (Datacenter ve Standart sürümler), Server 2012 R2, Windows Server 2012 ve Windows Server 2008 R2 Service Pack 1. domain etki alanını ele geçirebilir.


# Nasıl korunulur ?
- Domain Controllerlar için Enforcement Mode’u açmak
- Tanımlı ağlar dışından gelen MS-NRPC trafiği MFA/2FA/OTP gibi yöntemlerle trafiğin saldırgan tarafından kolayca istismar edilmesi zorlaştırılabilinir.

## Lateral Movement 
Enterprise Mitre ATT&CK / Command and Control 
Saldırganın hedefleri doğrultusunda ağda ilerlemesini sağlayan teknikleri içerir. Yanal Hareketi gerçekleştirmek için saldırganın kendi uzaktan erişim araçlarını kurması, daha gizli olabilecek yerel ağ ve işletim sistemi araçlarıyla meşru kimlik bilgilerini kullanması mümkündür. SSH ve RDP protokollerinin ele geçirilmesi, Windows uzaktan yönetimi, uzak hizmet oturumu ele geçirilmesi mümkündür.

## MS-NRPC(Netlogon Remote Protocol) 
The Netlogon Remote Protocol is a remote procedure call (RPC) interface that is used for user and machine authentication on domain-based networks. The Netlogon Remote Protocol RPC interface is also used to replicate the database for backup domain controllers (BDCs).
