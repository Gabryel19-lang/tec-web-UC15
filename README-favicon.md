Como gerar favicons (PNG / ICO) a partir do `favicon.svg`

Requisitos:
- ImageMagick instalado (comando `magick` no Windows, `convert`/`magick` em macOS/Linux).

Comandos (macOS / Linux):

```bash
# gera PNGs 16x16, 32x32, 48x48 e 180x180 (apple-touch)
# gera PNGs 16x16, 32x32, 48x48 e 180x180 (apple-touch)
magick convert favicon.svg -background none -resize 16x16 favicon-16.png
magick convert favicon.svg -background none -resize 32x32 favicon-32.png
magick convert favicon.svg -background none -resize 48x48 favicon-48.png
magick convert favicon.svg -background none -resize 180x180 apple-touch-icon.png

# gera favicon.ico combinando múltiplas resoluções
magick convert favicon-16.png favicon-32.png favicon-48.png favicon.ico

# OU use o script para gerar a partir de outro SVG (ex: favicon-anime.svg):
./generate-favicons.sh favicon-anime.svg anime
```

Comandos (Windows PowerShell / ImageMagick 'magick'):

```powershell
# ajuste o caminho se necessário e execute no diretório do projeto
magick favicon.svg -background none -resize 16x16 favicon-16.png
magick favicon.svg -background none -resize 32x32 favicon-32.png
magick favicon.svg -background none -resize 48x48 favicon-48.png
magick favicon.svg -background none -resize 180x180 apple-touch-icon.png
magick convert favicon-16.png favicon-32.png favicon-48.png favicon.ico
```

Uso em HTML (exemplos):
# ajuste o caminho se necessário e execute no diretório do projeto
magick favicon.svg -background none -resize 16x16 favicon-16.png
magick favicon.svg -background none -resize 32x32 favicon-32.png
magick favicon.svg -background none -resize 48x48 favicon-48.png
magick favicon.svg -background none -resize 180x180 apple-touch-icon.png
magick convert favicon-16.png favicon-32.png favicon-48.png favicon.ico
Write-Host "Favicons gerados: favicon-16.png, favicon-32.png, favicon-48.png, apple-touch-icon.png, favicon.ico"

# OU use o script PowerShell para gerar a partir de outro SVG (ex: favicon-anime.svg):
.\generate-favicons.ps1 -Svg favicon-anime.svg -OutPrefix anime
```

Se quiser, eu gero os PNGs e o ICO diretamente aqui — confirme se prefere que eu os crie no repositório (posso tentar gerar arquivos PNG/ICO automaticamente).