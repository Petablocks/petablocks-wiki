# petablocks-wiki

BookStack wiki configuration and customizations for [wiki.petablocks.com](https://wiki.petablocks.com).

## About BookStack

BookStack is a WYSIWYG wiki platform with a **Shelves → Books → Chapters → Pages** hierarchy. No Markdown required — contributors use a rich text editor. Players get a clean, searchable, mobile-responsive site.

It runs as a Docker container on PETABLOCKS-FEA backed by MariaDB on PETABLOCKS-DB.

## Structure

```
petablocks-wiki/
├── customizations/
│   ├── custom-head.html    # Injected into <head> — Inter font, brand colours
│   └── custom-footer.html  # Injected at body end — © PETABLOCKS branding
└── .env.example
```

## Applying Customizations

Customizations are synced automatically on deploy. To apply them manually in BookStack:

1. Go to **Admin → Settings → Customisation**
2. Paste `custom-head.html` into **Custom HTML Head Content**
3. Paste `custom-footer.html` into **Custom HTML Body End Content**

## First-Time BookStack Setup

1. BookStack starts via `petablocks-infra` docker-compose on the FEA VM
2. Browse to `https://wiki.petablocks.com`
3. Default credentials: `admin@admin.com` / `password` — **change immediately**
4. Admin → Settings → set App Name: `PETABLOCKS Wiki`
5. Upload your logo under Admin → Settings → Customisation → App Logo

## Recommended Role Setup

| Role | Who | Permissions |
|---|---|---|
| **Viewer** | All registered players | Read all public books |
| **Editor** | Staff | Create and edit pages in all books |
| **Admin** | Server management | Full access |

Set registration to open (or Discord OAuth via SAML) in **Admin → Settings → Authentication**.

## Deployment

Automatically deployed to `PETABLOCKS-FEA` via GitHub Actions on every push to `main`.
Requires the `DISCORD_WEBHOOK` secret in repository settings.
