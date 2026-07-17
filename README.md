# USGM TypeScript SDK

The official TypeScript / JavaScript SDK for the [US Global Mail API](https://docs.usglobalmail.com) — manage your virtual mailbox, scans, shipments, folders, addresses, and account programmatically.

## Installation

```bash
npm install @usgm/sdk
```

## Usage

```ts
import { UsgmClient } from "@usgm/sdk";

const client = new UsgmClient({ token: process.env.USGM_API_KEY });

// List mail in your mailbox
const mail = await client.mails.list();
console.log(mail);
```

The client exposes a sub-client per resource: `mails`, `scans`, `shipments`, `folders`, `addresses`, `bankAccounts`, `account`, and `sandbox`.

## Authentication

Pass your API key as `token`. Treat it like a password — keep it out of source control and client-side code. See the [documentation](https://docs.usglobalmail.com) for details.

## Documentation

- Guides: https://docs.usglobalmail.com
- API reference: https://docs.usglobalmail.com/api

## License

MIT
