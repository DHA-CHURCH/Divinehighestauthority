# Divine Highest Authority Website

A responsive React/Vite ministry website with a separate Book Library, Ministry Store, giving section, social links, and a deployment-ready Node/Express Paystack verification backend.

## Brand

- Deep navy blue
- Rich gold
- White
- Uses the supplied Divine Highest Authority logo in `client/public/dha-logo.jpg`

## Pages

Home · About · Sermons · Give · Book Library · Store · Contact

## Store categories (books intentionally excluded)

1. Audio Sermons
2. Video Teachings
3. Courses / Classes
4. Prayer & Declaration Packs
5. Devotionals
6. Event Replays

## Giving categories

Offering · Tithe · Prophet Offering · Change a Life · Kingdom Builders · Seed of Faith · Special Project Donation

## Social handles supplied

- TikTok: Divinehighestauthority.1
- Facebook: Chinwe Florence
- YouTube: Prophetessflora4170
- Instagram: Divinehighestauthority.1

## Before going live

1. Create and verify the ministry's Paystack account.
2. Put the Paystack secret key only in the backend host's environment variables.
3. Put the Paystack public key in the frontend payment implementation.
4. Configure the Paystack webhook to:
   `https://YOUR-BACKEND-DOMAIN/api/paystack/webhook`
5. Add a production database/order table before selling digital files. Do not rely on browser callbacks alone.
6. Add the actual book files, book covers, prices, and store products.
7. Replace the Facebook placeholder URL with the ministry's actual Facebook Page URL if different from the supplied personal account name.
8. Test in Paystack test mode, then switch to live keys only after successful end-to-end testing.

## Local development

### Frontend
```bash
cd client
npm install
npm run dev
```

### Backend
```bash
cd server
npm install
cp .env.example .env
npm start
```

The backend includes signed webhook validation and transaction verification. A production database and protected digital-download mechanism should be added before commercial launch.
