# Centsage delivery outcomes

## 1. C-based personal finance advisor server

- [x] Serve the website from a C11 HTTP server on the configured port, defaulting to port 3000 and binding to `0.0.0.0` for Preview.
- [x] Keep budgeting calculations, input validation, HTML rendering, and advisor response rules in C, with no external runtime library required beyond the C standard/POSIX socket APIs.
- [x] Avoid login, bank connections, database writes, and unnecessary retention of submitted financial data; process inputs only for the current request.

## 2. Accessible budget input and snapshot

- [x] Provide labeled fields for monthly take-home income, recurring expenses, flexible spending, debt payments, current savings, and a savings goal.
- [x] Validate that entered money values are numeric and non-negative, then show clear inline error messages when a value is invalid.
- [x] Show total committed spending, remaining monthly money, savings rate, spending breakdown, and a plain-language status label.
- [x] Show transparent calculation notes so a user can understand why each result appears.

## 3. Personalized savings guidance

- [x] Return practical rule-based contribution suggestions based on the user's remaining monthly money and goal.
- [x] Explain why the suggestion appears and distinguish educational guidance from professional advice.
- [x] Avoid unsupported claims, guarantees, or individualized investment/tax/insurance recommendations.

## 4. Conversational advisor interface

- [x] Provide a server-rendered advisor form for common budgeting and savings questions.
- [x] Use C-based response rules for questions about starting a budget, building a buffer, handling debt payments, and saving toward a goal.
- [x] Include a clear non-licensed-advisor disclosure near the conversation and in the page footer.

## 5. Responsive, minimal frontend

- [x] Use plain HTML forms and CSS with no frontend framework and no required JavaScript.
- [x] Include keyboard-visible focus states, readable contrast, responsive layouts, descriptive labels, and semantic headings.
- [x] Serve `/manus-routes.json` with the complete page route set before Preview starts.

## 6. Budget tracking and expense categorization

- [x] After a monthly snapshot, provide up to six expense rows with description, amount, and category controls.
- [x] Use C code to auto-categorize descriptions into Essentials, Flexible, Debt, or Other using keyword rules, while allowing an explicit category override.
- [x] Show tracked total, each category total, the matching monthly lane budget, remaining/over status, and the individual categorized expense list.
- [x] Keep tracking request/session-only with no database writes, and return clear validation when a row is incomplete or its amount is not greater than zero.

## 7. Delivery checks

- [x] Confirm the C compiler build, route manifest response, HTTP health response, and representative POST responses before handoff.
- [x] Save the finished website version to the managed repository after validation.
