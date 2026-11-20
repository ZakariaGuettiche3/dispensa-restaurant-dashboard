# Dispensa • Restaurant workspace

A bilingual React frontend for a single restaurant. The demo opens as the fictional owner. It includes cashier bills and payments, sales history, recipe costing, weighted-average inventory, suppliers and orders, expenses, reports, staff previews and appearance settings. All restaurant data is synthetic. Changes persist in this browser.

## Run the project

Extract the entire ZIP. To try the prebuilt frontend immediately, open `dist/index.html` in a browser. For development, use Node.js 20.19+ or 22.13+. In the project folder run:

```sh
npm ci
npm run dev
```

Open http://localhost:5173. The development server rebuilds source changes automatically. Reload the page to see them. Run `npm run build` to update the static distribution, `npm run lint` for static checks, and `npm test` for the production build and regression tests.

## How the code fits together

| Directory under src | Responsibility |
| --- | --- |
| app | Startup, building the current view model, and dispatching user actions |
| components | React application layout, shared navigation and screen rendering |
| hooks | React subscriptions, event listener lifecycle, screen controls and searchable lists |
| features | Screens and actions grouped by restaurant task, including cashier, expenses, inventory, reports and staff |
| domain | Framework-independent business rules, role projections and transaction handlers |
| services | Browser persistence, receipt attachments, image processing, file downloads and reporting |
| state | Session, transient view state, selectors and the observable React snapshot |
| navigation | Routes, access groups and the explicit screen registry |
| forms and templates | Shared bilingual form controls, validation, tables and existing HTML-based screen renderers |
| i18n and utils | Translation, formatting, escaping, color contrast, date and workbook helpers |
| data, styles and assets | Synthetic seed data, visual styling, icons and bundled menu images |

**Follow a staff preview through the code.** The directory component under `features/staff` uses `useSearchableList` for search and pagination. Its preview button dispatches the selected employee ID. The preview service requests the matching role projection from the domain, records the originating page, and navigates to the employee’s home screen. The workspace hook subscribes React to the updated view. Exiting preview restores the original page.

**Add a screen.** Put the view and its actions in its feature directory. Register its route in `navigation/screenRegistry.js` and its access group in `navigation/routes.js`. Existing screens can return escaped HTML through the shared template renderer. For a new React screen, return a typed screen model and select its component in `components/ScreenContent.jsx`, following Staff Directory. Use the domain layer for transaction rules, the storage service for persistence and paired English/Italian labels for UI text.

**Storage and compatibility.** The browser storage keys and saved restaurant record format match the previous React release. Reloading on the same origin retains demo records. File-based previews and localhost can have separate browser storage. Demo role switching is available in appearance settings. Use synthetic records only.
