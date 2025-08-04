# Tallaabooyinka Xallinta Dhibaatooyinka Network-ga (Network Troubleshooting Methodology)

## Dulucda Casharka
Dhibaatooyinka network-gu waa lama huraan. Xitaa network-yada ugu fiican way cilladoobaan. Waxa kala saara maamule network oo wanaagsan iyo mid kale waa sida uu u wajaho dhibaatada. Halkii laga ordi lahaa si fowdo ah oo la isku dayi lahaa wax kasta, waxaa jira habraac macquul ah oo tallaabo-tallaabo ah oo si weyn u kordhinaya fursadahaaga inaad si degdeg ah u hesho una xalliso asalka dhibaatada.

---

## 1. Muhiimadda Habraac Nidaamsan

Marka isticmaaluhu kuu yimaado oo uu ku yiraahdo, "Internet-ku ma shaqaynayo!", jawaabtaadu maahan inaad isla markiiba bilowdo inaad beddesho fiilooyinka. Waa inaad u fekertaa sida baaraha dembiyada oo kale. Waxaad u baahan tahay inaad ururiso caddeymo, sameyso mala-awaal, tijaabiso, oo aad meesha ka saarto waxyaabaha suurtogalka ah ilaa aad ka hesho dembiilaha dhabta ah.

Habraac nidaamsan wuxuu:
- Badbaadiyaa waqtiga.
- Yareeyaa khaladaadka.
- Hubiyaa inaadan ka boodin tallaabooyin muhiim ah.
- Kaa caawiyaa inaad wax ka barato dhibaatada si aysan mar kale u dhicin.

---

## 2. Lixda Tallaabo ee Xallinta Dhibaatooyinka Network-ga

Inta badan habraacyada xallinta dhibaatooyinka waxay raacaan qaab-dhismeedkan lixda tallaabo ah:

### Tallaabada 1: Aqoonso Dhibaatada (Identify the Problem)
Tani waa tallaabada ugu muhiimsan. Waa inaad si cad u qeexdaa dhibaatada. Si tan loo sameeyo, ururi macluumaad adigoo weydiinaya su'aalo:

- **Su'aalaha Isticmaalaha:**
  - "Maxaa si sax ah u shaqayn la'?" (Ma website gaar ah baa, mise internet-ka oo dhan?)
  - "Goormay dhibaatadu bilaabatay?"
  - "Ma adiga oo kaliya ayay dhibaatadani haysataa, mise dadka kale ee xafiiska jooga sidoo kale?" (Tani waxay kaa caawinaysaa inaad ogaato baaxadda dhibaatada).
  - "Ma jiraan wax isbeddelo ah oo dhacay ka hor intaysan dhibaatadu bilaaban?" (Software cusub, qalab cusub, iwm.).

- **Hubintaada Hordhaca ah:**
  - Hubi calaamadaha muuqda: Fiilooyinka ma ku xiran yihiin? Nalalka router-ku ma shidan yihiin?
  - Isticmaal aaladaha aasaasiga ah: `ping`, `ipconfig`/`ifconfig`.

### Tallaabada 2: Samee Mala-awaal ku Saabsan Sababta Suurtogalka ah (Establish a Theory of Probable Cause)
Marka aad macluumaadka ururiso, samee liis mala-awaal ah oo ku saabsan waxa sababi kara dhibaatada, adigoo ka bilaabaya kan ugu fudud uguna macquulsan.

- "Mala-awaal: Fiilada network-ga ayaa ka go'an."
- "Mala-awaal: Kombiyuutarku ma helin IP Address sax ah oo ka yimid DHCP."
- "Mala-awaal: DNS server-ku ma shaqaynayo."
- "Mala-awaal: Router-ka ayaa cilladoobay."
- "Mala-awaal: Shirkadda isgaarsiinta (ISP) ayaa leh dhibaato."

### Tallaabada 3: Tijaabi Mala-awaalka si aad u Go'aamiso Sababta (Test the Theory to Determine Cause)
Hadda, mid-mid u tijaabi mala-awaalladaada, adigoo ka bilaabaya kan ugu fudud.

- Tijaabo: Fiiri fiilada. Ma ku xiran tahay? Ku tijaabi deked kale.
- Tijaabo: Ku qor `ipconfig`. IP-gu ma yahay mid sax ah (sida 192.168.1.x) mise waa mid iskiis loo sameeyay (sida 169.254.x.x, oo muujinaya dhibaato DHCP)?
- Tijaabo: `ping 8.8.8.8`. Haddii uu shaqeeyo, laakiin `ping google.com` uusan shaqayn, markaas dhibaatadu waa DNS.
- Tijaabo: ping-garee Default Gateway-gaaga (router-ka). Haddii uusan shaqayn, dhibaatadu waxay u dhaxaysaa adiga iyo router-ka.
- Tijaabo: Haddii wax walba oo gudaha ahi ay u muuqdaan inay sax yihiin, wac ISP-ga.

Marka aad hesho mala-awaal shaqeeya oo xaqiijiya sababta, u gudub tallaabada xigta. Haddii mala-awaalkaagu uu khaldan yahay, meesha ka saar oo u gudub kan xiga ee liiskaaga.

### Tallaabada 4: Samee Qorshe Wax-qabad si aad u Xalliso Dhibaatada una Hirgeli Xalka (Establish a Plan of Action & Implement the Solution)
Marka aad ogaato sababta, samee qorshe aad ku xalliso.

- Sababta: Fiilo go'an. Xalka: Dib u xir fiilada.
- Sababta: Dhibaato DHCP. Xalka: Isku day inaad cusboonaysiiso IP-ga (`ipconfig /release` kadibna `ipconfig /renew`). Haddii aysan shaqayn, dib u kici router-ka.
- Sababta: Dhibaato DNS. Xalka: Si ku-meel-gaar ah u beddel DNS server-kaaga una beddel mid dadweyne sida 8.8.8.8.
- Sababta: Router-ka oo cilladoobay. Xalka: Dib u kici router-ka. Haddii aysan taasi shaqayn, waxaa laga yaabaa inuu u baahdo in la beddelo.

### Tallaabada 5: Xaqiiji Shaqaynta Buuxda ee Nidaamka (Verify Full System Functionality)
Marka aad hirgeliso xalka, ha iska tegin. Xaqiiji in dhibaatadii si buuxda loo xalliyay.

- Hubi in isticmaaluhu uu hadda geli karo internet-ka.
- Hubi inuu geli karo adeegyadii kale ee network-ga.
- La soco nidaamka dhowr daqiiqo si aad u hubiso in dhibaatadu aysan soo laaban.

### Tallaabada 6: Diiwaan-geli Natiijooyinka, Tallaabooyinka, iyo Natiijada (Document Findings, Actions, and Outcomes)
Tani waa tallaabo ay dad badani iska indha-tiraan laakiin aad muhiim u ah.

- Qor waxa ay ahayd dhibaatadu.
- Qor tallaabooyinkii aad qaadday si aad u ogaato sababta.
- Qor xalkii aad hirgelisay.

Diiwaangelintani waxay kaa caawinaysaa adiga iyo asxaabtaada inaad si degdeg ah u xallisaan dhibaato la mid ah haddii ay mustaqbalka dhacdo. Waxay abuurtaa "database aqooneed" (knowledge base).

---

## Habka OSI Model ee Xallinta Dhibaatooyinka

Hab kale oo caan ah oo loo wajaho xallinta dhibaatooyinka waa in la isticmaalo OSI Model. Waxaad ka bilaabi kartaa hoos (Bottom-Up) ama kor (Top-Down).

### Bottom-Up (Hoos-ka-Kor)
- **Physical (Lakabka 1):** Fiilooyinku ma ku xiran yihiin? Nalalku ma shidan yihiin?
- **Data Link (Lakabka 2):** Switch-ku ma shaqaynayaa? Kaarka network-gu ma cilladaysan yahay?
- **Network (Lakabka 3):** Ma jiraa IP Address sax ah? Router-ku ma shaqaynayaa?

Habkani wuxuu ku fiican yahay marka aad ka shakisan tahay dhibaato hardware ah.

### Top-Down (Kor-ka-Hoos)
- **Application (Lakabka 7):** Browser-ku ma shaqaynayaa? Ma isku dayday browser kale?
- **Transport (Lakabka 4):** Firewall-ka kombiyuutarku ma xannibayaa barnaamijka?

Habkani wuxuu ku fiican yahay marka aad ka shakisan tahay dhibaato software ah oo ku kooban hal barnaamij.