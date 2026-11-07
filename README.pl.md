# BlockBreach — Ready or Not × Minecraft

[English](README.md) · [Русский](README.ru.md) · **Polski**

**Minecraft Java działa obok Ready or Not, a jego bloki, moby i wybuchy pojawiają się w obrazie Ready or Not** — na
właściwej głębokości, pod interfejsem, z oświetleniem dopasowanym do sceny. Buduj osłony w środku szturmu, poszczuj
podejrzanych zombie, wysadź ścianę TNT.

**Pobieranie:** [Releases](https://github.com/ImmortalSouull/BlockBreach/releases) → `BlockBreach-1.0.0.zip` →
uruchom `BlockBreach.exe`. Budowanie ze źródeł: [BUILDING.md](BUILDING.md).

## Co robi
- **Minecraft w obrazie.** Kamera Ready or Not steruje kamerą Minecrafta; klatka Minecrafta jest wkomponowana w obraz
  Ready or Not według bufora głębi (dodatek ReShade), z oświetleniem i mgiełką dopasowanymi do mapy.
- **Poziom Ready or Not w Minecrafcie.** Podłogi, schody i ściany stają się niewidzialnymi barierami, więc moby
  Minecrafta chodzą po każdej mapie, wchodzą po schodach i przechodzą przez drzwi.
- **Tryb budowania (NumPad 0).** Mysz, kółko i 1–9 trafiają do Minecrafta: stawiaj bloki na podłodze Ready or Not,
  używaj dowolnego przedmiotu. **E** otwiera kreatywny ekwipunek Minecrafta ze wszystkimi przedmiotami. Każdy
  postawiony blok to twarda ściana w Ready or Not (gracze i SI się o nią opierają, pociski się zatrzymują).
- **Dwie gry walczą.** Strzały, miecz, TNT, creepery i fajerwerki z kuszy ranią ludzi Ready or Not; Twoja broń zabija
  moby Minecrafta (strzały w głowę się liczą); podejrzani i Twój oddział strzelają do zombie; zombie polują na
  podejrzanych, funkcjonariuszy i na Ciebie.
- **Każda mapa** dostaje własną część świata Minecrafta: to, co zbudujesz, zostaje na tej mapie.

## Wymagania
- Windows 10/11, karta graficzna, która uciągnie obie gry (sprawdzone: RTX 4050 w laptopie, ~65–85 fps przy
  1920×1200).
- **Ready or Not** (Steam), sprawdzone na buildzie 133804. Tylko gra jednoosobowa.
- **Minecraft: Java Edition** z oficjalnym Minecraft Launcherem (Microsoft Store / aplikacja Xbox lub klasyczny).
  BlockBreach używa Minecrafta 26.3 z Fabric Loader 0.19.5 we własnym folderze gry; launcher sam pobierze grę przy
  pierwszym uruchomieniu.

## Instalacja
1. Uruchom **BlockBreach.exe**. Sam znajdzie Ready or Not (przez Steam) i Minecraft Launcher.
2. **DEPLOY** — instaluje wszystko (≈30 MB). Pliki, które już były w folderze Ready or Not, trafiają do kopii
   zapasowej.
3. **READY** — otwiera Minecraft Launcher z wybranym profilem *BlockBreach*: naciśnij tam **PLAY**. Gdy Minecraft otworzy
   swój świat, BlockBreach uruchomi Ready or Not w DirectX 11 przez Steam.
4. Zacznij dowolną misję. Minecraft się w niej pojawi.

Windows SmartScreen może ostrzec o nieznanym wydawcy (exe nie jest podpisany): *Więcej informacji → Uruchom mimo to*.
Niektóre antywirusy oznaczają `dwmapi.dll` / `dxgi.dll` (przez nie ładują się UE4SS i ReShade): tak działają oba
narzędzia.

## Sterowanie
| Klawisz | |
|---|---|
| NumPad 0 | Tryb budowania wł./wył. (mysz, kółko i 1–9 trafiają do Minecrafta) |
| LPM / PPM | Tryb budowania: niszcz, atakuj, strzelaj z łuku / postaw blok, użyj przedmiotu |
| 1–9, kółko | Tryb budowania: slot paska |
| ŚPM | Tryb budowania: wybierz blok, na który patrzysz |
| E | Tryb budowania: ekwipunek Minecrafta (E lub Esc zamyka) |
| Strzał | Twoja broń trafia też moby Minecrafta |
| F5 | Minecraft w obrazie wł./wył. |
| F6 | Wyrównaj podłoże + bloki testowe przed Tobą |
| F7 | Rysuj Minecrafta pod / nad interfejsem |

Pasek: jajo zombie, diamentowy miecz, kusza (+ fajerwerki w drugiej ręce), łuk, TNT, krzesiwo, jajo creepera, blok
trawy, fajerwerki.

## Ustawienia
BlockBreach → **SETTINGS**: rozdzielczość renderowania Minecrafta (domyślnie 75 %: więcej FPS, a pikselowe bloki
wyglądają tak samo), czy moby na Ciebie polują, czy Twój oddział walczy z mobami. Stosowane przy następnym
uruchomieniu Ready or Not.

## Odinstalowanie
BlockBreach → **INSTALL → UNINSTALL** (lub Windows *Aplikacje i funkcje → BlockBreach*). Wszystko znika, pliki z kopii
zapasowej wracają, profil Minecrafta jest usuwany; Twój świat Minecrafta zostaje, jeśli o to poprosisz.

## Rozwiązywanie problemów
- Nie widać Minecrafta w Ready or Not: Ready or Not musi działać w **DirectX 11** (użyj READY albo Steam → *Play Ready
  or Not (DirectX 11)*), a Minecraft musi być w swoim świecie, zanim zaczniesz misję. F5 przełącza obraz.
- Logi: `…\Ready Or Not\ReadyOrNot\Binaries\Win64\ue4ss\UE4SS.log`, `…\ue4ss\Mods\RoNPassthrough\history.log`,
  `…\Win64\ReShade.log`; Minecraft: `%LOCALAPPDATA%\BlockBreach\minecraft\logs\latest.log`.
- Po aktualizacji Ready or Not gra może przestać ładować UE4SS: BlockBreach → INSTALL → REPAIR i sprawdź, czy jest
  aktualizacja BlockBreach.
- Inna instalacja ReShade lub UE4SS w tym samym folderze trafia do kopii zapasowej i jest zastępowana, dopóki
  BlockBreach jest zainstalowany.

## Podziękowania
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) (MIT) — system skryptów dla Unreal Engine.
- [ReShade](https://reshade.me) (BSD 3-Clause) autorstwa crosire — API dodatków, w którym działa kompozytor.
- [Fabric Loader i Fabric API](https://fabricmc.net) (Apache 2.0).
- Przykład *mc-gta5-passthrough* autorstwa rehan (MIT) — mod przekazywania Minecrafta i kompozytor, na których to
  zbudowano.
- Czcionki: Oswald, Roboto Condensed, JetBrains Mono, Press Start 2P (SIL Open Font License).
- Zrobione z Claude (Anthropic) w Claude Code: kod, instalator, grafika (proceduralna) i testy.
- Projekt fanowski. Niezwiązany z VOID Interactive, Mojang Studios ani Microsoft. *Ready or Not* i *Minecraft* to znaki
  towarowe ich właścicieli.

Tłumaczenie przygotowane przy pomocy AI.

Licencja: własny kod BlockBreach jest na licencji MIT (zob. LICENSE). Części zewnętrzne zachowują swoje licencje
(THIRD_PARTY_NOTICES.md).
