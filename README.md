## Next.js App Router Course – Starter

This is the starter template for the **Next.js App Router Course**. It contains the base code for the dashboard application.

For more details, see the [course curriculum](https://nextjs.org/learn) on the Next.js website.

---

### Progress Checkpoints
- **Optimized Images** – [Left off here](https://nextjs.org/learn/dashboard-app/optimizing-fonts-images#why-optimize-images)
- **Layouts and Pages** – [Left off here](https://nextjs.org/learn/dashboard-app/creating-layouts-and-pages)
- **Request Waterfalls** – [Read more](https://nextjs.org/learn/dashboard-app/fetching-data#what-are-request-waterfalls)
- **Streaming** – [Read more](https://nextjs.org/learn/dashboard-app/streaming)

---

## React Suspense

[Streaming a Component](https://nextjs.org/learn/dashboard-app/streaming#streaming-a-component)

React Suspense lets you specify a **fallback UI** that’s displayed while the main component is loading.  
- While loading, the fallback (often a skeleton) is shown.  
- Once data is ready, React swaps in the real UI.  
- This process of progressively replacing placeholders is referred to as **streaming** in React.

---

## [CH 10: Partial Prerendering](https://nextjs.org/learn/dashboard-app/partial-prerendering)
*(Skipped – not advisable for production in this case.)*

---

## [CH 11: Adding Search and Pagination](https://nextjs.org/learn/dashboard-app/adding-search-and-pagination)

**Debouncing**  
- Delays execution of a function until a short period after the last user input.  
- Prevents multiple unnecessary calls (e.g., database queries) while typing.

**Pagination**  
- Splits data into pages to improve performance and navigation.

---

## [CH 12: Mutating Data](https://nextjs.org/learn/dashboard-app/mutating-data)

### Creating an Invoice
- Used **Zod** to typecast `amount` from string to number.
- Used `revalidatePath` from `next/cache` to keep browser cache correct.
- Redirected after creation to return the user to the invoices page.

### Updating an Invoice
- Ensure `page.tsx` is in the correct nested folder structure.  
- Pass ID to server action using TypeScript’s `bind` as needed.

### Deleting an Invoice
- Basic delete with SQL and path revalidation.

---

## [Handling Errors](https://nextjs.org/learn/dashboard-app/error-handling)

**General Error Handling**
- Place `error.tsx` at the root of the relevant route (e.g., `dashboard/invoices`).
- Use `reset` to navigate back after an error.
- For uncaught exceptions, you can `throw new Error("message")`.

**404 Handling**
- Use `notFound()` from Next.js to display a styled "Not Found" component.

---

## [Improving Accessibility](https://nextjs.org/learn/dashboard-app/improving-accessibility)

- Added ESLint accessibility plugin (`eslint-plugin-jsx-a11y`).
- Use `pnpm lint` to check for accessibility issues.

### Client-Side Validation — Key Takeaways
1. **Runs in the browser before data is sent**  
   - Native HTML5 attributes like `required`, `type="number"`, and `pattern` prevent submission until conditions are met.
2. **Helpful but not secure**  
   - Instant feedback, but can be bypassed — always pair with server-side validation.
3. **Accessibility limitations**  
   - Some assistive technologies (ATs) may not announce native messages.  
   - Consider custom, AT-friendly error messaging.

### Server-Side Validation — Key Takeaways
- **Runs on the server** – Zod schema validation happens before any database action.
- **Consistent rules** – Works for all submission methods (UI, API, scripts).
- **More secure** – Cannot be bypassed by disabling JavaScript or editing the DOM.
- **Single source of truth** – Centralized schema for all validation requirements.
- **Error handling with `useActionState`** – Returns structured `errors` and `message` for the UI.
- **Accessible feedback** – ARIA attributes like `aria-describedby` and `aria-live` make server errors screen reader-friendly.
- **Pairs with client-side checks** – Client checks offer instant feedback, but server-side remains the final authority.

---

## [Adding Authentication](https://nextjs.org/learn/dashboard-app/adding-authentication)
*(Not yet started.)*
