# Releases / Lançamentos

- `AURALIS-Setup.exe`: instalador web (pequeno, menos de 1 MB). Baixa os dados do jogo da pasta `dados/` deste repositório.
- `SHA256.txt`: SHA-256 do instalador. Confira antes de executar (veja o README principal).

The installer is a small web installer (< 1 MB) that downloads the game data from `dados/`. `SHA256.txt` holds its SHA-256.

Como conferir / How to verify (PowerShell):

```powershell
Get-FileHash .\AURALIS-Setup.exe -Algorithm SHA256
```
