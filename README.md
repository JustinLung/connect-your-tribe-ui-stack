> _Fork_ deze leertaak en ga aan de slag. Onderstaande outline ga je gedurende deze taak in jouw eigen GitHub omgeving uitwerken. De instructie vind je in: [docs/INSTRUCTIONS.md](docs/INSTRUCTIONS.md)

# 🚀 Visitekaartje V2 - UI Stack

<!-- Geef je project een titel en schrijf in één zin wat het is -->

Deze repo laat verschillende schetsen zien voor de UI stack van mijn visitekaartje.

- Loading state
- Empty state
- Error State

## ✍️ Breakdown & Wireflow Schetsen

### 📭 Empty State
![Empty state](https://github.com/JustinLung/connect-your-tribe-ui-stack/blob/main/docs/empty-state.png?raw=true)

### 🚫 Error State
![Error state](https://github.com/JustinLung/connect-your-tribe-ui-stack/blob/main/docs/error-state.png?raw=true)

### ⏳ Loading State
![Loading State](https://github.com/JustinLung/connect-your-tribe-ui-stack/blob/main/docs/loading-state.png?raw=true)

## 💻 Code

<!-- Leg de code uit die je gebruikt om de verschillende states van de UI-Stack te tonen -->

HTML

```html
<noscript>
  <img src="assets/memoji.png" alt="justin's memoji" />
  <h2>Oops... Something went wrong</h2>
  <p>Please turn on Javascript to see this page.</p>
</noscript>
```

JavaScript

```js
async function getMember() {
    try {
        const res = await fetch(`${API_URL}/member`)
        if(res.ok === true) {
            hidePreloader();
        }
        const member = await res.json()
        render(member)
    }
    catch (err) {
        error();
        throw new Error(err);
    }
}
```

## Licentie

![GNU GPL V3](https://www.gnu.org/graphics/gplv3-127x51.png)

This work is licensed under [GNU GPLv3](./LICENSE).
