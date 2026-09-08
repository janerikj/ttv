# ttv – SVT Text-TV i terminalen

En snabb, minimalistisk och tangentbordsstyrd terminalklient för SVT Text-TV skriven i Python.

## Krav

* Python 3
* `requests` (`pip install requests`)

## Installation

Gör skriptet körbart och placera det gärna i din sökväg (`PATH`), exempelvis `~/.local/bin/`:

```bash
chmod +x ttv
ln -s "$(pwd)/ttv" ~/.local/bin/ttv
```

## Användning

```bash
# Starta interaktivt på sida 100
ttv

# Starta interaktivt på en specifik sida
ttv 104

# Skriv ut en sida direkt till stdout och avsluta
ttv -p 130
ttv --print 130

# Spara en sida till textfil utan ANSI-färgkoder
ttv -p 130 --no-color > sida130.txt

# Visa hjälptext
ttv -h
```

## Navigering i klienten

| Tangent | Funktion |
| :--- | :--- |
| `0-9` | Slå in ett tresiffrigt sidnummer direkt |
| `Pil upp` / `u` | Välj föregående länk |
| `Pil ned` / `d` | Välj nästa länk |
| `Enter` | Följ vald länk |
| `Pil vänster` / `p` | Föregående sida |
| `Pil höger` / `n` | Nästa sida |
| `+` / `-` | Bläddra mellan undersidor |
| `r` | Ladda om aktuell sida (tvinga ny hämtning) |
| `Esc` | Rensa inmatning / avmarkera länk |
| `q` / `Ctrl+C` | Avsluta klienten |

> **Obs:** Hämtade sidor sparas i minnet (cache) under sessionen för snabb navigering fram och tillbaka utan onödiga nätverksanrop. Tryck på `r` för att rensa cachen för aktuell sida och hämta igen.

## AI-deklaration

Detta projekt har utvecklats och färdigställts med Google Gemini som AI-kodstöd.

## Licens

Detta projekt är licensierat under [MIT-licensen](LICENSE) – fri att använda, modifiera och distribuera.
