<svelte:head>
    <script async src="https://www.googletagmanager.com/gtag/js?id={key}"></script>
</svelte:head>
<script>
    export let page
    export let key

    if (typeof window !== "undefined") {
        window.dataLayer = window.dataLayer || []
        window.gtag = function gtag() {
            window.dataLayer.push(arguments)
        }
        window.gtag("js", new Date())
        window.gtag("config", key, { 'send_page_view': false })
    }

    $: {
        if (typeof gtag !== "undefined"){
            window.gtag("config", key, {
                page_path: page?.url?.pathname,
            });
        }
    }
</script>
