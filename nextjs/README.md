# Next.js SSR

## Exercise goals
The goal of this exercise is to create a minimal microblog application using SSR features.
The final app should have a timeline view, presenting the available posts stored in our JSON backend and a Compose view
to create new posts.

## Getting started
You can start the dev setup by running:

```shell
npm run dev
```

**Remember to start your JSON backend as well, (see root README for details).**

## Tasks

1. Create an empty timeline page with Gatsby using the provided starter setup - see [Next.js routing](https://nextjs.org/docs/app/building-your-application/routing) for more information. You can use hardcoded data for this step. We will be connecting to the backend later. Have a look at `backend/storage/database.json` for seed data. The timeline should present a list of posts, showing at least the message and the author's name. If you're feeling fancy you can also add avatars based on the `userId` using a service such as https://pravatar.cc/.
2. Fill your timeline view with actual backend data using [server-side data fetching](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating). We provided a small API connection layer [here](src/models/posts.server.ts), so you can focus on SSR topics. Make sure your browser is not making HTTP Requests against the JSON backend to verify the data is actually loaded server-side.
3. Add a second route to your app presenting a compose view. The compose view should consist of a simple form with an input field and submit button. It is fine to simply hardcode the submitting user's id for this since we will not bother with user management. Upon submitting the form, the new post should be saved to the backend.
4. Bonus task - support Markdown!
   a) Extend your timeline view to display the post message as parsed markdown. We recommend using [react-markdown](https://github.com/remarkjs/react-markdown) for this.

   b) Extend your compose view by adding a Markdown preview next to the input showing a parsed version of the input text. Think about where the markdown parsing happens and how it differs between timeline and compose view and the implications.
