Ez az „Arany Standard” Műszaki Dokumentáció, amely a RoomFinder Buddy 3.0 webapplikáció stabilizálásához és a Gemini Canvas környezetbe való integrálásához készült. Ez a dokumentum az „Okos Jegyzetelés” folyamat során feltárt összes kritikus adatot, vizuális auditot és technikai követelményt egyesíti.
---
📑 RoomFinder Buddy 3.0 – Műszaki és Implementációs Dokumentáció
1. Projekt Összefoglaló és Kontextus
Cél: Egy interaktív, párokra optimalizált szobakereső asszisztens, amely segít szűrni a hirdetéseket, elemzi a piaci adatokat és biztonsági protokollt nyújt a bérléshez.
Céldátum: 2026. március 31. (Dinamikus visszaszámláló a UI-ban).
Fókuszterület: London és környéke (M25 bázis), Peterborough irányú elmozdulás.
Filozófia: AI-szövetség, radikális őszinteség, strukturált döntéshozatal.
---
2. Technikai Architektúra (Az „Arany Standard” – GPT Stable)
Az alkalmazás stabilitását a következő technológiai stog (stack) biztosítja:
Frontend: Alpine.js (állapotkezelés), Tailwind CSS (styling), Lucide Icons (ikonkészlet).
Vizualizáció: Chart.js (reszponzív szórásdiagramok és oszlopdiagramok).
AI Motor: Gemini 1.5/2.0 Flash (v1beta endpoint), Google Search Grounding támogatással.
Stabilitási réteg („Légzsák”):
Demo mód: Ha nincs API kulcs vagy hálózati hiba lép fel, a rendszer heurisztikus alapú elemzésre vált (nem omlik össze).
x-cloak: CSS szabály a villódzás (FOUC) elkerülésére az Alpine.js betöltése előtt.
---
3. UI/UX Hierarchia és Funkcionális Audit (Tab-alapú lebontás)
A. Home (Kezdőlap)
Vizuális elemek: 4 db információs kártya (Max bérleti díj, Páros bérlés, Scam szűrő, Proximity).
Státusz számlálók: Mentett hirdetések, „Maybe”, „Approved” és „Rejected” státuszok valós idejű kijelzése.
AI Analyzer: Cím és szöveg beviteli mező, „Elemzés” és „Törlés” gombok.
B. Data (Térkép & Statisztika)
Grafikonok:
Szórásdiagram: Ár (£/hét) vs. Komfort szint.
Oszlopdiagram: Átlagos bérleti díjak régiók szerint.
Interaktív Panel: Város-specifikus adatok, AI Insight gomb valós idejű Google Search-szel.
C. Protocol (Biztonság)
48h Biztonsági Terv: 4 lépéses harmonika-menü (Kapcsolatfelvétel, Megtekintés, Szerződés, Beköltözés).
Viewing Checklist: 7 pontos interaktív, pipálható lista a helyszíni szemléhez.
SitRep: AI-alapú dilemma-feloldó modul.
D. Templates (Kommunikáció & Admin)
AI Reply Generator: Üzenet írása az ügynököknek.
Statikus Sablonok: 3 db előre megírt, azonnal másolható üzenet.
Rendszereszközök: Master Report másolása, JSON Export/Import, Smoke Tests (fejlesztői funkciók).
---
4. A „Gemini Regresszió” – Tanulságok és Hibák
A korábbi kísérletek során a Gemini „kontextus-fáradtsága” miatt fellépő hibák, amiket el kell kerülni:
UI Butítás: A kártyák számának csökkentése (4-ről 2-re), akciógombok elhagyása.
Hibakezelés hiánya: 401-es hiba esetén a UI lefagyott a Demo mód hiánya miatt.
Grafikon torzulás: Fix magasságú konténerek (h-[250px]) használata a reszponzív megoldások helyett.
Hiányzó modulok: A súlyozott pontozórendszer (Scam/Fit súlyok) és a Viewing Checklist teljes elhagyása.
---
5. Implementációs Protokoll (A „Szent Grál” Szabályok)
Zéró-Inferencia Szabály: Csak a GPT „Stable” kód szerkezetét használjuk bázisként. Ne írj át CSS-t vagy Alpine.js logikát „tisztítás” címszóval.
Sebészi Integráció: Az AI hívásokat (fetchGeminiWithRetry) úgy kell beépíteni, hogy a meglévő UI elemek (loading indikátorok, eredményjelzők) érintetlenek maradjanak.
Környezeti Integráció:
apiKey = "" (A Canvas injektálja).
Endpoint: v1beta Gemini Flash.
Retry logika: Exponenciális visszalépés (1s, 2s, 4s, 8s, 16s).
Vizuális Integritás: Kötelező a kód végén az összes nyitott </div> és <script> tag lezárása a Preview funkció megőrzéséhez.
---
6. AI Modul Specifikációk (Gemini Canvas-re hangolva)
Listing Analyzer: Heurisztikus elő-elemzés (helyi JS) + Gemini mélyelemzés.
Town Insight: Kötelező Google Search grounding (tools: [{ "google_search": {} }]).
SitRep: Radikális őszinteség üzemmód, radikális objektivitás.
Reply Generator: Udvarias, de határozott üzleti angol stílus.
---
Záró megjegyzés: Ez a dokumentum a fejlesztési folyamat során „élő” marad, és minden módosítási kör előtt referenciaként szolgál, hogy ne veszítsünk el többé funkciókat vagy vizuális minőséget.
Vége a dokumentációnak.
---
