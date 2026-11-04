# IncuBYTE — original source export

This is the actual source of your existing IncuBYTE website, copied from the
source commit used for its successful version 3 deployment. It is not a recreation.
All five original tracked files are byte-for-byte unchanged. Only this README,
`vercel.json`, and `EXPORT-MANIFEST.json` were added to the export.

## What is included

| File | Purpose | Status |
| --- | --- | --- |
| `dist/index.html` | Original page, sidebar, header, dialog, and script links | Unchanged |
| `dist/style.css` | Original colors, typography, spacing, cards, responsive layouts, and animations | Unchanged |
| `dist/data.js` | Original sample projects, reviews, mentors, pilots, and challenges | Unchanged |
| `dist/app.js` | Original navigation, inline SVG icons, views, forms, interactions, local storage, and exports | Unchanged |
| `.openai/hosting.json` | Original Sites hosting configuration, retained for provenance | Unchanged; unused by Vercel |
| `vercel.json` | Serve the existing `dist` directory without building it | Added for Vercel |
| `EXPORT-MANIFEST.json` | Original commit, version, and file hashes | Added for verification |
| `README.md` | Local preview, deployment, and preservation instructions | Added documentation |

The original app is plain HTML, CSS, and JavaScript. There are no React components,
`package.json`, npm dependencies, server functions, or separate image assets in
this version. Icons and illustrations are generated within the original HTML,
CSS, and JavaScript. The existing Google Fonts reference for **DM Sans** and
**Manrope** is preserved exactly; viewing those fonts requires internet access.

All eight existing sections are retained:

1. Overview — `#overview`
2. Betaverse launchpad — `#launchpad`
3. Validation dashboard — `#validation`
4. Micro-mentorship — `#mentorship`
5. Pilot opportunities — `#pilots`
6. Startup pipeline — `#pipeline`
7. Tester portfolio — `#portfolio`
8. Partners & plans — `#partners`

The QueueLess, ReCircle, CampusFlow, and SkillSwap sample projects and their
existing sample data are included in `dist/data.js`.

## Open and run in VS Code on Windows

1. Download the ZIP and choose **Extract All** in File Explorer.
2. In VS Code, select **File → Open Folder** and open the extracted **IncuBYTE**
   folder. Its immediate contents should include `vercel.json` and `dist`.
3. Select **Terminal → New Terminal**. Keep the terminal in this folder.
4. If Python is installed, run:

   ```powershell
   py -m http.server 5500 --bind 127.0.0.1 --directory dist
   ```

5. Open **http://127.0.0.1:5500/** in your browser. Keep the terminal running.
   Press **Ctrl+C** in the terminal to stop the preview.

If the `py` command is unavailable but Python is installed as `python`, use:

```powershell
python -m http.server 5500 --bind 127.0.0.1 --directory dist
```

Alternatively, with the VS Code **Live Server** extension installed, right-click
`dist/index.html` and choose **Open with Live Server**. Either preview serves the
same original website files. A local HTTP preview is preferable to double-clicking
the HTML because browser storage behavior can vary for `file:` URLs.

You do not need `npm install` or a React build to run this website.

## Deploy to Vercel from this folder

The source needs no conversion. Vercel should serve the existing `dist` directory.
The included `vercel.json` sets the output directory and skips the build step.

1. Install [Node.js LTS](https://nodejs.org/) if Node and npm are unavailable.
   Restart VS Code after installation so the terminal picks up the new PATH.
2. Open the **IncuBYTE** folder's terminal and sign in to your own Vercel account:

   ```powershell
   npx --yes vercel@latest login
   ```

3. Start the production deployment:

   ```powershell
   npx --yes vercel@latest --prod
   ```

4. If prompted, select your Vercel account, create a new project, choose your
   preferred available project name, and keep the code directory as **`./`**.
5. Check these settings if Vercel asks for them:

   | Setting | Value |
   | --- | --- |
   | Framework Preset | Other |
   | Project / Root Directory | The folder containing `vercel.json` |
   | Build Command | Empty; skip the build |
   | Output Directory | `dist` |
   | Install Command | None needed |
   | Environment variables | None required by this source |

6. Open the production URL returned by Vercel. Its assigned `vercel.app` address
   will not contain `chatgpt.site`. The exact address is allocated during deployment.

If Windows PowerShell blocks `npx.ps1`, run the same commands with `npx.cmd`
instead of `npx`. No change to the website files is needed.

For later updates, deploy again from the same linked folder using
`npx --yes vercel@latest --prod`. The original Sites website is unaffected.

### Optional: deploy through GitHub

Upload this folder's contents to a GitHub repository, then import that repository
in Vercel. Keep `vercel.json` at the selected root and use the settings above.
Upload the actual extracted files, not the ZIP. You do not need to connect
GitHub when using the CLI method.

Official references, checked on 17 October 2026:

- [Vercel build configuration](https://vercel.com/docs/builds/configure-a-build)
- [Vercel deployment command](https://vercel.com/docs/cli/deploy)

## Data when you change the URL

The existing sample data is part of the source and will be available on Vercel.
Your personal browser activity is stored under `incubyte-product-v3` in
`localStorage`. Browsers keep separate storage for each origin, so data saved on
the original domain does not automatically appear on localhost or Vercel.

Before leaving the original site, click **Campus workspace → Export your
workspace** to save a JSON backup of your personal activity. The unchanged app
does not have an import button. Keep the backup if you want to restore that
activity separately. No browser-local user data is embedded in this source ZIP.

Existing prototype behavior is preserved: forms and requests remain local demo
interactions, sample metrics remain illustrative, and the app has no shared
backend or live request delivery. Authentication or access controls supplied by
the original hosting platform are not part of these application source files.

## Verify that the original source is unchanged

Source version: **3**

Source commit: **`1ccc2d7ede79e2520daea484825a3f5dc32985c7`**

`EXPORT-MANIFEST.json` lists the SHA-256 of every original file. For example,
check the original stylesheet from PowerShell with:

```powershell
Get-FileHash .\dist\style.css -Algorithm SHA256
```

Compare its hash to the corresponding manifest entry. The export was checked
against the committed source and every original file inside the ZIP. Both
JavaScript files passed Node syntax checks. No browser visual test or Vercel
deployment was performed as part of preparing this export.

The original files have deliberately not been reformatted, split, renamed, or
rewritten, so the visual design and application behavior remain in their
original source form.
