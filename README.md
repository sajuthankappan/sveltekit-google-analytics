# Svelte Google Analytics

Google analytics for svelte-kit

# How to use

## Install
Install @sajuthankappan/sveltekit-google-analytics
```
npm i @sajuthankappan/sveltekit-google-analytics
```

## Sample usage

In your svelte component (say, __layout.svelte)
```
<script>
    import GoogleAnalytics from '@sajuthankappan/sveltekit-google-analytics';
    import { page } from '$app/stores';
    const gaKey = import.meta.env.VITE_GA_KEY;
</script>

<GoogleAnalytics {page} key={gaKey}/>
```

## Credits

[sapper-google-analytics](https://www.npmjs.com/package/sapper-google-analytics)

## Create package & publish

```bash
npm run package
npm publish ./package --access public
```

Note: Publishing to be done only by the npm package owner.
