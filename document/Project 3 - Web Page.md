# Project 3 - Web Page

**Programming Merit Badge · HTML + JavaScript**

**Goal:** Build a pack-check page from parts. Then add one more part of your own.

Open [JSFiddle](https://jsfiddle.net). Paste into the **HTML** box. Leave the other boxes empty. Click **Run**.

## 1. The parts

| Part | Code | What you see |
| :--- | :--- | :--- |
| Title | `<h2> ... </h2>` | Big words |
| Label | `<label> ... </label>` | Words next to a box |
| Box | `<input>` | Where you type |
| Button | `<button> ... </button>` | Click to start |
| Answer | `<h3> ... </h3>` | The page talks back |
| Menu | `<select> ... </select>` | A drop-down list |

## 2. Stack the page

Paste this, then click **Run**.

```html
<h2>Scout Pack Check</h2>

<label>Temperature (°F): </label>
<input type="number" id="tempInput">

<button onclick="checkGear()">Check Gear</button>
<h3 id="resultOutput"></h3>
```

You should see a title, a box, and a button. The button does nothing yet.

- [ ] I see a title, a box, and a button

## 3. Add one more part

Paste **one** of these under the title. Click **Run** again.

```html
<p>Night hike</p>
```

```html
<select id="weather">
  <option>Sunny</option>
  <option>Rain</option>
  <option>Snow</option>
</select>
```

```html
<label><input type="checkbox" id="raining"> Raining</label>
```

The new part shows up on the page. The button does not use it yet.

- [ ] I added one extra part

## 4. Make the button decide

Paste this under the answer line, still in the HTML box. Click **Run**.

```html
<script>
function checkGear() {
  let temp = document.getElementById("tempInput").value;
  let answer = document.getElementById("resultOutput");

  if (temp == "") {
    answer.textContent = "Type a temperature first.";
  } else if (temp < 50) {
    answer.textContent = "Pack a heavy jacket and a hat.";
  } else {
    answer.textContent = "Pack a light jacket and extra water.";
  }
}
</script>
```

`getElementById` finds the part with that id. `textContent` changes the words in the answer.

Type **32** and click the button. Then type **75**.

- [ ] Cold and warm show different words
- [ ] A counselor saw it

**Stuck?** The id on the box and the name inside `getElementById` have to be the same word. Ask a counselor.

---

### Bonus: Night mode (not required)

Add a second button under **Check Gear**. This button changes the whole page.

```html
<button onclick="nightMode()">Night mode</button>

<script>
function nightMode() {
  document.body.style.backgroundColor = "#14233a";
  document.body.style.color = "white";
}
</script>
```

`document.body` is the whole page. `style.backgroundColor` paints it.

- [ ] The page turns dark when I click **Night mode**
