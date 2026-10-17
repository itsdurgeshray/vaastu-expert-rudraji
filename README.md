# Pandit Rudra Prasad Upadhyay: Website Guide

A single page website (`index.html` + `assets/`). There is no server, no database and no login. Every booking goes to Panditji's WhatsApp, and every payment goes straight to his UPI.

The site is in three languages: English, Hindi and Nepali. Visitors switch from the language button in the header.

## 1. Before going live

Open `index.html` and edit only the **SITE SETTINGS** block near the top. Text has three versions: `en`, `hi`, `ne`.

| Setting | Status |
|---|---|
| `whatsappNumber`, `phoneDisplay`, `phoneTel` | Set to +91 80112 84911. The number is never shown on the page until a visitor has sent a request. |
| `upiId`, `upiName` | **Placeholder.** Put Panditji's real UPI ID here. |
| `upiQrImage` | Optional. Save his QR from PhonePe/GPay as `assets/upi-qr.png` and write `"assets/upi-qr.png"`. |
| `serviceArea`, `hours` | **Placeholder** (Varanasi). Change to his real city and hours. |
| `stats` | **Placeholder.** Real years of practice and real numbers only. |
| `services` | Fees are placeholders. Use `""` to hide a fee and show "shared on WhatsApp". |
| `testimonials` | **The six reviews are samples.** Replace with real words from real clients, with their permission. |

Also:
- The introduction under "Meet your guide" is a draft. Search `about.` in the file to change all three languages together.
- After the site has its final web address, change `assets/og-image.jpg` in the `og:image` line to the full address so WhatsApp shows Panditji's photo when the link is shared.
- Artwork (lotuses, yantras, Vastu mandala, service illustrations) is drawn in code, so there are no image rights to clear. The only photo is Panditji's portrait.

## 2. How a booking works

1. The visitor taps a service card or **Book a Consultation**.
2. Four quick steps: service, meeting type (visit, video or phone), day (as soon as possible, this week, or a date), and their name. City is asked only for home visits. No phone number is asked: Panditji sees it in WhatsApp.
3. They tap **Send on WhatsApp**. WhatsApp opens with the message already written:

```
🙏 Namaste Panditji,
I would like to book a consultation.

Booking ID: RP2410-482
Service: Home Vastu
Meeting: Visit at my home or site
Preferred day: As soon as possible

Name: ...
City / Area: ...
```

4. The website shows a thank-you screen with the booking ID, what happens next, the UPI QR for later payment, and (only here) Panditji's phone number in case WhatsApp did not open.
5. Panditji replies to confirm the time and dakshina. The visitor pays by UPI and sends the screenshot in the same chat.

No advance payment means no refunds to manage.

## 3. Panditji's setup on his phone (one time, about 20 minutes)

Use the free **WhatsApp Business** app on his number.

**Labels** (long press a chat, Label): 🟡 New request, 🟢 Confirmed, 🔵 Paid, ⚪ Done. Tapping a label lists those chats. This is his booking register.

**Quick replies** (Settings, Business tools, Quick replies). Typing `/` in a chat shows them:

- `/pakka`: 🙏 नमस्ते जी, आपका परामर्श ____ को ____ बजे पक्का है। दक्षिणा ₹____ है। कृपया UPI से भुगतान करके स्क्रीनशॉट भेज दें।
- `/naksha`: कृपया घर का नक्शा या हाथ से बना स्केच, मुख्य द्वार की दिशा, और हर कमरे की फ़ोटो भेज दें।
- `/prapt`: 🙏 दक्षिणा प्राप्त हुई, धन्यवाद। ____ को मिलते हैं।

**Away message**: an auto reply outside his hours, e.g. "नमस्ते, पंडित जी आपको शीघ्र उत्तर देंगे।"

## 4. Payments and records

- Best option: a free merchant UPI account (PhonePe Business, Paytm for Business or Google Pay for Business). It gives a QR, a voice alert for every payment, and a daily statement that serves as his record.
- Every payment note includes the Booking ID (e.g. `Dakshina RP2410-482`), so a payment can be matched to its WhatsApp chat.
- Visitors from Nepal may not have UPI. If many come from Nepal, add an eSewa, Khalti or Fonepay QR and mention it in the confirmation reply.

## 5. Putting it online (free)

- **Netlify Drop**: go to app.netlify.com/drop and drag this folder in.
- **GitHub Pages**: in the repository settings, Pages, choose the `main` branch and root folder.

A custom domain (about ₹800 a year) can be added later.
