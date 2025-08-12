## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

Left off on optimized Images [here](https://nextjs.org/learn/dashboard-app/optimizing-fonts-images#why-optimize-images)

Left off on Layouts and pages
[here](https://nextjs.org/learn/dashboard-app/creating-layouts-and-pages)

[Request Waterfalls](https://nextjs.org/learn/dashboard-app/fetching-data#what-are-request-waterfalls)

[Streaming](https://nextjs.org/learn/dashboard-app/streaming)

## React Suspense

[Streaming a component](https://nextjs.org/learn/dashboard-app/streaming#streaming-a-component)

React Suspense lets you specify a fallback React element that is shown while the main component is loading. In this example, the fallback is a UI skeleton.

In the actual component, instead of immediately rendering with props, we can perform business logic or data fetching inside it. While that data is loading, the fallback (skeleton) is displayed. Once the data arrives, React swaps the fallback for the actual UI component.

This process—where parts of the UI stream in and replace placeholders—is referred to as **streaming** in React.

## **[CH 10 Partial Prerendering](https://nextjs.org/learn/dashboard-app/partial-prerendering)**

Skipped since not advisable in production...

## [Ch11 Adding Search and Pagination](https://nextjs.org/learn/dashboard-app/adding-search-and-pagination)

### [Capture the user's input](https://nextjs.org/learn/dashboard-app/adding-search-and-pagination#1-capture-the-users-input)

### [Debouncing](https://nextjs.org/learn/dashboard-app/adding-search-and-pagination#best-practice-debouncing)

Debouncing is the practice of delaying the execution of a function until after a specified period of inactivity. For example, in a search bar, a timer is reset on each keystroke. When the user pauses typing—indicating they’ve likely finished their query—the function (such as a database search) runs. This helps prevent multiple unnecessary calls and improves performance.

### [Adding Pagination](https://nextjs.org/learn/dashboard-app/adding-search-and-pagination#adding-pagination)

## [ch12 Mutating Data](https://nextjs.org/learn/dashboard-app/mutating-data)

### Creating an Invoice

Highlights: Used Zod to typecast amount to a number, since it populates as a string. Used revalidatePath method from 'nextcache' in order to store correct cache in client browser to prevent unnecessary rerenderings. used a redirect so that when that is complete, the action of creating an invoice, user is taken back to invoices page.

### [Updating an Invoice](https://nextjs.org/learn/dashboard-app/mutating-data#updating-an-invoice)
