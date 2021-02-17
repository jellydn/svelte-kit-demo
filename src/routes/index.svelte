<script context="module">
  export const load = async ({ fetch }) => {
    const query = `
            query Doubled($x: Int) {
                double(number: $x)
            }
		`;

    const variables = {
      x: 19,
    };

    const response = await fetch("/graphql", {
      body: JSON.stringify({ variables, query }),
      headers: {
        Authorization: "Token ABC123",
        "Content-Type": "application/json",
      },
      method: "POST",
    });

    const { data, errors } = await response.json();

    if (errors)
      throw new Error(errors.map(({ message }) => message).join("\n"));

    return {
      props: {
        doubled: data.double,
      },
    };
  };
</script>

<script lang="ts">
  import Counter from "$components/Counter.svelte";
  export let doubled: number;
</script>

<main>
  <h1>Hello world!</h1>
  <h2>The API said {doubled}</h2>

  <Counter count={doubled} />
  <p>
    Visit the <a class="text-blue-600 underline" href="https://svelte.dev"
      >svelte.dev</a
    > to learn how to build Svelte apps.
  </p>
</main>

<style lang="scss">
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    @apply text-center;
    @apply p-4;
    @apply mx-auto;
  }

  h1 {
    @apply text-red-600;
    @apply uppercase;
    @apply text-6xl;
    @apply font-thin;
    @apply leading-tight;
    @apply my-16 mx-auto;
    @apply max-w-xs;
  }

  p {
    @apply max-w-xs;
    @apply my-8 mx-auto;
    @apply leading-snug;
  }

  @screen sm {
    h1 {
      @apply max-w-none;
    }

    p {
      @apply max-w-none;
    }
  }
</style>
