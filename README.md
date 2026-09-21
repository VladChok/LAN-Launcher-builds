# LAN-Launcher-builds

Публикуемые манифесты сборки модов для [LAN-Launcher](https://github.com/VladChok/LAN-Launcher)
(приватный). Здесь только JSON с URL + SHA-512 и, позже, наш собственный
`lan-client` Fabric-мод. Чужие `.jar` сюда не кладутся — они скачиваются с
Modrinth / maven.fabricmc.net по ссылкам из манифеста.

- `current.json` — указатель на текущую стабильную сборку (`stable`, `manifest`).
- `builds/vN.json` — версионированные манифесты (никогда не переписываются;
  новая сборка = новый файл + обновлённый `current.json`).

Лаунчер читает `current.json` по HTTPS с `raw.githubusercontent.com`, проверяет
структуру (`formatVersion` = 1) и пути, сверяет файлы по размеру и SHA-512.
