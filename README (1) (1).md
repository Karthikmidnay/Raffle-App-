# Conclave Raffle

A prize draw app for live events. It is a single file that opens in a web browser. Nothing to install, no account, no internet connection needed.

You load a list of attendees, enter your sponsors and prizes, and draw winners on a projector in front of an audience. Nobody can win twice. The same file works for every event you run.

*Contributed by Karthik C, Midnay.*

---

## What is in this folder

| File | What it is |
|---|---|
| `raffle-app.html` | The app. This is the only file you need to run a draw. |
| `Conclave-Raffle-Guide.pdf` | The illustrated user guide. Give this to whoever is operating the draw. |
| `sample-attendees.csv` | An example attendee list. Copy its layout for your own. |
| `README.md` | This file. |
| `CHECKLIST.md` | A short run sheet for the day of the event. |

---

## Quick start

1. Copy `raffle-app.html` onto the laptop that will drive the projector, and double-click it.
2. Click **Sponsor & prize** and enter your event name, sponsors and prizes.
3. Click **Import attendees (CSV)** and choose your list, or drag the file onto the window.
4. Click **Full screen (projector)**.
5. Press **Draw a winner**, or the space bar, or a presentation clicker.

The app opens with a demo list already loaded, so you can press the button straight away to see how it works before setting anything up.

---

## The eight steps

### 1. Open the app

Double-click `raffle-app.html`. All the controls sit on the grey bar along the very bottom of the window. That bar is for you, the operator — everything above it is what the audience sees.

Your setup is remembered by the browser, so open the same file from the same place each time. Moving to another folder or another laptop? Use **Save settings file** to carry your setup across.

### 2. Set up your event

Click **Sponsor & prize**.

| Box | What to put in it |
|---|---|
| Main title | The big name across the screen, usually your event name |
| Event name | Used for the browser tab and the name of the file you download at the end |
| The two small lines | Optional. Leave them empty and they will not appear. |

The screen changes as you type. If the panel is in the way, click **Dock right** in its corner and it moves aside so you can watch.

### 3. Add your sponsors and prizes

Still in **Sponsor & prize**. Use the dropdown at the top to pick which sponsor you are editing, and **Add** to create more.

For each sponsor: name, the prize written as a plain sentence, how many winners, and optionally a logo and a background image. **Use for every sponsor** copies one background to all of them.

**Save** keeps your changes. **Cancel** undoes them.

### 4. Prepare your attendee list

A CSV file with a heading row. From Excel or Google Sheets: *File → Save as* (or *Download*) and choose **CSV**.

```
ticket_id,name,company,email,phone
T-1001,Anita Raghavan,Northwind,anita@example.com,98450 11111
T-1002,Mohan Das,Brightfold,mohan@example.com,98450 22222
T-1003,Fatima Sheikh,Cedar & Co,fatima@example.com,98450 33333
```

| Column | Needed? | Notes |
|---|---|---|
| `ticket_id` | Yes | Different for every person. Also accepts `ticket`, `ticket_no`, `ticket number`, `id`, `registration_id`, `booking_ref`. |
| `name` | Yes | Also accepts `full_name`, `attendee`, `delegate`, `member`, `guest_name`. |
| `company` | No | Also `organisation`, `employer`, `firm`. |
| `checked_in` | No | If present, rows saying `no` or `false` are left out of the draw. |
| anything else | No | Phone, job title, T-shirt size, table number — all kept and shown in the winners list, never on the projector. |

Capital letters and spaces in headings are fine — `Ticket ID` and `Full Name` both work. Files saved from Excel work, including ones separated by semicolons or tabs.

### 5. Import the list

Click **Import attendees (CSV)**, or drag the file onto the window.

Check the bottom right. It should say *"Loaded 240 attendees."* and then show your file name and count. If it still says **built-in demo list**, the file was refused and the message says why.

### 6. Change how it looks (optional)

Click **Themes & designs**. Nothing here affects the draw or the attendee list, so you can change it at any time, even between draws.

Twelve themes, eight layouts, ten winner-reveal styles, your own accent and background colours, fonts, your event logo, and a background image. Dock or minimise the panel to see the screen while you choose.

### 7. Run the draw

Connect the projector and set the display to **mirror**. Click **Full screen (projector)** so the room sees only the draw, not your browser tabs.

Pick the sponsor from the **Drawing for** row under the main screen — it shows how many prizes each has left. Then press **Draw a winner**, the space bar, or a clicker.

- **Winner not in the room?** Press **Winner absent — redraw**. The prize is cancelled and you draw again. That person cannot be drawn a second time and is recorded as absent.
- **Sponsor finished?** The button reads *All prizes drawn*. Tap the next sponsor and carry on.

### 8. Save the winners

Click **Total winners**. Every winner is listed under their sponsor with all the details from your file. Press **Download the list (CSV)**, or **Copy the list** to paste into an email.

> **Do this before you close the tab.** Winners are not stored anywhere. Closing or refreshing the browser clears them.

---

## How the draw is kept fair

| Rule | What it means |
|---|---|
| Nobody wins twice | Once drawn, a person is out of the pool for the rest of the event, whichever sponsor they won from. |
| The winner is picked first | The result is decided the instant you press the button, before the animation starts. A slow laptop cannot change who wins. |
| Every ticket is equal | Selection uses the browser's secure random number generator. There is no weighting and no way to influence it from the screen. |
| One entry each | Duplicate ticket numbers in your file count once. |
| The count is on screen | The audience can see the number of tickets going down after each draw. |

---

## Your attendees' data

The attendee list stays inside the browser tab and nowhere else. It is never uploaded, never saved to the computer, and never included in your settings. Closing the tab discards it.

**Delete imported file** removes it immediately, along with the winners drawn from it.

What is remembered is only your setup: event name, sponsors, prizes, logos and the look you chose.

---

## Every button on the bar

| Button | What it does |
|---|---|
| Import attendees (CSV) | Loads your list of people |
| All sponsors | Shows every sponsor and their remaining prizes |
| Sponsor & prize | The main editor |
| Total winners | The full record, and the download |
| Themes & designs | Colours, layouts, fonts, logos, backgrounds |
| Delete imported file | Removes the attendee list and its winners |
| Sound on / off | The ticks, beeps and fanfare |
| Countdown on / off | The three-two-one before each draw |
| Light / dark | Quick switch between two colour schemes |
| Full screen (projector) | Fills the display. Press `Esc` to come back. |
| Clear winners | Puts everyone back in the pool. Use after a practice draw. |

**Keyboard:** `Space` or `Enter` draws a winner. `Esc` closes the open panel.

**Panels:** every panel has **Dock right**, **Minimise** and **Close** in its corner, and can be dragged by its title. Docked, the stage behind stays live so you can see your changes.

---

## If something goes wrong

| What you see | What to do |
|---|---|
| "Needs a ticket and a name column" | The message lists the headings found in your file. Rename one column to `ticket_id` and one to `name`, save as CSV again, re-import. |
| It still says "built-in demo list" | Your file was refused. Read the message in the bottom right for the reason. |
| The draw button is greyed out | That sponsor has no prizes left. Choose another in the **Drawing for** row. |
| A logo looks wrong | Use a PNG with a transparent background, or an SVG. |
| The page looks plain and broken | You are opening it from inside a zip folder. Extract the file first. |
| My setup has disappeared | You are opening a different copy of the file, or the browser cleared its storage. Use **Load settings file** if you saved one. |
| The audience can see my browser tabs | You are not in full screen. Click **Full screen (projector)**. |

---

## Technical notes

- Runs entirely offline. Fonts are embedded in the file; there are no network requests at any point.
- Works in Chrome, Edge, Firefox and Safari on any desktop operating system.
- Tested with attendee lists from 3 to 500 people. The draw takes the same time whatever the list size.
- Settings are stored in the browser's local storage under one key, and can be exported as a `.json` file.
- Respects the operating system's reduced-motion setting: the animation is skipped and the winner is revealed immediately.
