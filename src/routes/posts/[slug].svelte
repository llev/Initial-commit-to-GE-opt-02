<script context="module">
    export async function load({ page }) {
        const Hello = await import(`../../posts/${page.params.slug}.md`)
        return {
            props: {
                Hello: Hello.default,
                date: Hello.metadata.date,
                title: Hello.metadata.title,
                author: Hello.metadata.author
            }
        }
    }
</script>

<script>
    // import Hello from '../../posts/hello.md'
    // export let Hello
    export let title
    export let date
    export let author
</script>

<!-- <Hello /> -->


<div class="container px-5 mx-auto lg:px-32">
    <div class="flex flex-col w-full mx-auto mb-2 text-left lg:w-3/4 ">
      <p class="my-4 text-lg leading-snug tracking-tight text-blue-400 lg:w-2/3"> {date} </p>
      <h1 class="mb-2 text-3xl font-black tracking-tighter text-black lg:text-5xl md:text-4xl">{title}</h1>
      <p class="mt-4 text-lg leading-snug tracking-tight text-blueGray-400 lg:w-2/3"> {author} </p>
    </div>
  </div>