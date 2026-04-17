# Stockria Print Helper — User Guide

Stockria Print Helper is a small desktop app for Mac. Install it on the
computer connected to your label printer. When you click Print in
Stockria, Print Helper takes the label, renders it sharp, and sends it
straight to your printer — no OS print dialog, no barcode artifacts, no
multi-page overflow.

This guide covers Mac only. A Windows version is coming.

---

## What you need

- A Mac running macOS 12 (Monterey) or newer.
- A Stockria account with sign-in details.
- A label printer — plugged in by USB or on your Wi-Fi / ethernet.
- About 2 minutes.

---

## 1. Download the app

1. In Stockria, open **Inventory → Labels**.
2. In the top-right of the Labels page, click **Download Print
   Helper**. A `.dmg` file downloads to your Mac.

If you don't see the button, refresh the page. If it still doesn't
show, ask whoever set up your Stockria account to confirm the release
feed is configured.

---

## 2. Install it

1. Open the `.dmg` you just downloaded.
2. A window opens with the Print Helper icon. **Drag it into the
   Applications folder** shown next to it.
3. Close the window. You can eject the `.dmg` from Finder's sidebar.

---

## 3. First launch (important)

The alpha version isn't code-signed by Apple yet. macOS will complain
the first time. You only need to do this once.

1. Open **Applications** in Finder.
2. **Right-click** (or Control-click) on **Stockria Print Helper** →
   choose **Open**.
3. A dialog appears: "macOS cannot verify the developer..." Click
   **Open** again.

The app launches. macOS remembers your choice. From now on you can open
it the normal way.

If you just double-click without right-clicking first, macOS shows a
red warning and refuses to open. Close the warning and follow the
right-click method above.

---

## 4. Sign in to Stockria

When Print Helper opens for the first time, a **Welcome** window
appears.

1. Click **Sign in to Stockria**.
2. Print Helper shows an 8-character code, e.g. `AB4X-7KP9`.
3. Your web browser opens to a Stockria page asking for the code. (If
   it doesn't open automatically, copy the URL shown in Print Helper
   and paste it into your browser.)
4. Enter the code. Click **Approve device**.
5. Go back to Print Helper. It automatically moves on to the next
   step.

The code expires after 10 minutes. If you miss the window, click Sign
in again.

---

## 5. Add your printer

Print Helper looks for printers installed on your Mac.

1. Click **Scan for printers**.
2. Pick yours from the list. Click **Add**.

If your printer isn't in the list:

- **USB printer:** Plug it in, turn it on, then in Mac **System
  Settings → Printers & Scanners**, click **+** and add it. Back in
  Print Helper, click **Scan for printers** again.
- **Network printer (Zebra, TSC, Godex etc. with Ethernet):** In
  Print Helper, click **Add network printer** instead. Type the
  printer's IP address (check the printer's label or menu — usually
  something like `192.168.1.50`). Leave the port at `9100`. Click
  **Add printer**.

---

## 6. Print a test label

Print Helper offers to print one. Click **Print test label**.

Your printer should start within a few seconds. Check the label:

- The whole layout should fit on one label — no cut-offs.
- The barcode should be crisp (no grey shading or jagged bars).
- Try scanning the barcode with your barcode scanner to confirm it
  reads.

If anything looks wrong, go to **Printers → Configure** for that
printer and use the calibration options in section 10.

---

## 7. Print from Stockria

Once Print Helper is running, printing from the Stockria web app is
one click.

1. Open Stockria in your browser.
2. Go to **Inventory → Labels**.
3. Select one or more products.
4. Click **Print**.

A small green "Print Helper connected" badge appears next to the
Print button when Print Helper is running. If you see it, prints go
through Print Helper automatically — no browser print dialog.

If the badge isn't there, the browser uses its own print dialog
instead. Check that Print Helper is still running (look at your Mac's
menu bar — see section 9).

---

## 8. Make your own label layout

Print Helper ships with one layout: a 51×25 mm (2×1 inch) bin label.
You can edit it or create new ones.

1. In Print Helper, click **Templates**.
2. Click **New template** (or **Edit** on an existing one).

Inside the editor:

- **Top bar:** label name, width, height, DPI (use 300 for most
  thermal printers, 203 for older ones, 600 for high-end models).
- **Left: Add** — click **Text**, **Barcode**, **QR code**, or
  **Box** to drop a new element onto the label.
- **Middle:** drag elements around. They snap to mm coordinates.
- **Right: Inspector** — edit the selected element's properties:
  - **Bind to** — choose a product field like SKU, Name, Price. The
    element fills in with that product's data when printed. Leave
    blank for a barcode to use the product's barcode field; for
    text, you can type a fixed string instead.
  - Size, font, position, etc.

To delete an element: hover it in the **Layers** list on the left
and click the **✕**, or select it and press **Delete**.

Click **Save template** when done. It saves to your Stockria account
so other machines with Print Helper can use the same layout.

Keyboard: `Cmd`+`S` saves without closing.

---

## 9. The menu-bar icon

Print Helper runs quietly in the background. Look at the top of your
screen for a small icon in the Mac menu bar.

Click it for quick actions:

- **Open window** — bring the main Print Helper window back up.
- **Open logs folder** — opens a Finder window with log files (for
  support — see section 12).
- **Export support bundle…** — saves one file with system info and
  recent logs that you can email to support.
- **Quit Print Helper** — stops the app completely.

The menu also shows how many printers you have set up and how many
jobs are waiting.

---

## 10. If your labels don't look right

Open **Printers**, find your printer, click **Configure**.

- **X offset / Y offset (mm)** — if the print starts too far left,
  right, up, or down on the label, adjust these. Positive X shifts
  print right; positive Y shifts down. Start with ±1 mm.
- **Darkness (0–30)** — only for thermal printers. If the print is
  too light, increase. If it's smudging or burning through, decrease.
  Most printers work fine around 15.
- **Test pattern** — prints a calibration label with an alignment box
  and a sample barcode. Use it after each change to check.

Save when the test label lines up with the label stock.

---

## 11. Updating

Print Helper checks for updates automatically every few hours. When a
new version is ready, you'll see a notification in the app's title
bar: **"Update x.x.x ready"** with a **Restart now** button.

To check manually: open **Settings → About → Check for updates**.

Clicking **Restart & install** quits the app, installs the new
version, and re-opens it. Your settings, printers, and templates
stay.

---

## 12. Something's wrong — what to do

### The app won't open on first launch

You didn't right-click → Open the first time. Go back to section 3.

### My printer isn't in the list after Scan

1. In Mac **System Settings → Printers & Scanners**, confirm your
   printer is listed and shows as **Idle** (not Offline).
2. Click **Scan for printers** in Print Helper again.
3. Still missing? Check the USB cable or power first, then reach out
   to support with an export support bundle (section 9).

### My label prints but the barcode won't scan

Either the barcode is too small, too fuzzy, or too dark:

1. Try a different scanner first — some cheap ones can't read
   Code128 at small module widths.
2. In the template, make the barcode taller (≥ 10 mm) and wider. If
   the SKU is very long, consider switching to QR instead.
3. In Printers → Configure, reduce **Darkness** a few steps.

### The label overflows or doesn't fit

You picked the wrong label size for your stock. In the template
editor top bar, set **W** and **H** to the actual size of your label
stock in millimetres. A 2×1 inch label = 51×25 mm.

### The Print button in Stockria doesn't route through Print Helper

Look for the green "Print Helper connected" badge on the Labels page
in Stockria. If it's missing:

1. Check Print Helper is running — look for the menu-bar icon.
2. Make sure the Mac running Stockria in the browser is the **same
   Mac** running Print Helper (or on the same Wi-Fi network).
3. Quit Print Helper from the menu-bar icon, re-open it from
   Applications. Wait 10 seconds. Refresh Stockria.

### I want to un-pair a device / log Print Helper out

In Stockria, go to **Settings → Print Helper**. You'll see every
machine that's signed in. Click **Revoke** next to the one you want
to log out. That machine's Print Helper stops working until someone
signs it in again.

---

## Getting support

1. In Print Helper, click the menu-bar icon → **Export support
   bundle…**. Save the file.
2. Email it to support with:
   - What you were trying to do.
   - What happened instead.
   - The printer make and model.
   - A photo of the bad print if relevant.

The bundle contains app logs and system info only — no product data,
no passwords. You can open it in a text editor and read it yourself
before sending.
