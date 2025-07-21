# qrProfile

A simple, modern static website to create and share personal profiles with QR codes. Built with HTML, CSS, and vanilla JavaScript. No frameworks required.

## Features
- **Create Profile:** Users can enter their name, phone, blood group, and address.
- **SheetDB Integration:** Data is saved to a Google Sheet via [SheetDB](https://sheetdb.io/).
- **Profile URL & QR Code:** Generates a unique profile URL and QR code for sharing.
- **PDF Download:** Download the QR code as a PDF using [jsPDF](https://github.com/parallax/jsPDF).
- **Profile Viewer:** Anyone can view a profile by visiting the profile URL.
- **Mobile Responsive:** Clean, modern, and responsive UI.

## Live Demo
Deploy easily on [Vercel](https://vercel.com/) or any static hosting provider.

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/bappy-3/qrProfile.git
cd qrProfile
```

### 2. Edit the SheetDB Endpoint
- Open `index.html` and `profile.html`.
- Replace the value of `SHEETDB_ENDPOINT` with your own SheetDB API endpoint:
  ```js
  const SHEETDB_ENDPOINT = 'https://sheetdb.io/api/v1/oggwndcfwe81g'; // <-- Replace this
  ```
- Make sure your SheetDB fields match the form fields (`fullName`, `phone`, `bloodGroup`, `address`).

### 3. Deploy to Vercel
- If you have [Vercel CLI](https://vercel.com/docs/cli) installed:
  ```bash
  vercel --prod
  ```
- Or, import the repo at [vercel.com/new](https://vercel.com/new) and follow the prompts.

## Usage
- Go to `index.html` to create a profile and get a QR code.
- Scan or share the QR code/profile URL. Anyone can view the profile at `profile.html?phone=YOUR_PHONE_NUMBER`.

## Customization
- **Styling:** Edit `styles.css` for colors, spacing, and layout.
- **Form Fields:** Change or add fields in `index.html` and update the SheetDB integration accordingly.
- **PDF/QR:** Uses [jsPDF](https://github.com/parallax/jsPDF) and [QRCode.js](https://davidshimjs.github.io/qrcodejs/) via CDN.

## Credits
- [jsPDF](https://github.com/parallax/jsPDF) for PDF generation
- [QRCode.js](https://davidshimjs.github.io/qrcodejs/) for QR code generation
- [SheetDB](https://sheetdb.io/) for Google Sheets API

## License
MIT 