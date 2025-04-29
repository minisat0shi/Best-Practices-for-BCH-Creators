# Best-Practices-for-BCH-Creators
A focus on what creators in the BCH community can do to improve their search rankings, relevance, and sharing!






Paste from BCR:
I did not think of a better place to post this, but I wanted to start writing these things down in a place that could be referenced from in the future.

In brief, this is meant to be a thread of tips and other ideas that I've found have worked to improve the social/online state of BCH, but in no means is meant to be an ultimatum or perfect standard. My hope is that we can collect a bunch of these ideas, refine them, and as a community work to improve our standing.


***Search Engine Ranking Improvement***
SEO is incredibly important, however BCH naturally will struggle with this until we are covered more frequently in the media. I will touch on this topic a little below, but this doesn't mean there aren't things we can do!

**What Can EVERYONE do?**
Google, Bing, and DuckDuckGo all have feedback tools for search engines.
Search for basic things like "What is Bitcoin Cash" or just "Bitcoin Cash" or maybe some BCH tool, then find the feedback button (typically right side), and fill out the feedback. If it is bad, let them know it is not a helpful return of results. If there is some good stuff, say it was helpful but then still type comments of how they could improve. You can specifically request for certain domains to appear higher as they are more relevant.
Try to avoid comments saying they are biased or hijacked, but focus on comments saying "out of date" and these other sites are more relevant. An example of a recent feedback I submitted was this: "Certain sources such as bitcoincash.org, whatisbitcoin.cash, and discover.cash should absolutely be included higher in the rankings. The by and large majority of the sources shown here are displaying highly out of date information."

Believe it or not, this helps. Submitting this feedback has changed the search rankings in bing and duckduckgo for sites, including my own.
![IMAGE 2025-04-29 13:24:19|386x500](upload://4968tSE0ucCUzeOToF4ABi4uSn4.jpeg)


**What can CREATORS do?**
All creators should take an hour or so to create Bing and Google Webmaster accounts, claim ownership of their sites, and familiarize themselves with the console. It's fairly intuitive, but the most important tools are the manual indexing and SEO issues/suggestions. Through here you can manually control your sitemap and other tools that are incredibly important for SEO.
Additionally, particularly with Bing, the search engine will not generally automatically pull your favicon to display in web results. To get it displayed, you must contact their webmaster team through the console. This process is fairly painless, just a simple email requesting them to add your favicon (provide the web link to it) to bing search results, and within a few days or weeks they will complete the request! When they do this, they also appear to put the site through some sort of approval which boosts rankings (as I have noticed).

Web owners should check out tools like Lighthouse to see how their page response, loading, etc works and suggestions for improvement: https://pagespeed.web.dev

Also, there are guidelines for proper meta tags and otherwise to handle search engines and to help ensure your intended title/description is shown. Titles should be 40-60 characters and descriptions between 140-160 characters. Google and other search engines will often truncate titles and descriptions, or even fully replace with random text grabs if titles and descriptions are longer (or, though less often, shorter!) than these lengths.

There are also schemas you can do. Grok and other AIs can help generate effective Schemas for your website, but they are important for SEO and how results are displayed. Here's another site that's helpful: https://technicalseo.com/tools/schema-markup-generator/

Canonical links, favicons, webapp compatibility are all also important. But these can be found in the <head> sample below.


|||I will include a <head> tag example below that will show some of this|||


***Search Engine/Twitter/Telegram/Facebook Cards***

This is an important enhancement for sites to get better traction. By default, sharing websites on Twitter/X and other platforms will not generate a site preview or card. Even Search Engine views can be improved! With just a little bit of HTML, we can dictate what we want these platforms to show. Below is a snippet (and at the bottom of this post will be a sample <head> tag with all info).

```
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://minisatoshi.cash">
    <meta property="og:title" content="What is Bitcoin Cash (BCH)? | The Freedom Money Revolution">
    <meta property="og:description" content="Discover Bitcoin Cash (BCH): a fast, low-cost, decentralized cryptocurrency designed for everyone. Join the freedom revolution! | minisatoshi.cash">
    <meta property="og:image" content="https://minisatoshi.cash/images/minisatoshicash.jpg?v=2">
    <meta property="og:image:alt" content="minisatoshi.cash homepage image.">
    <meta property="og:article:section" content="Information">
    <meta property="og:article:tag" content="Bitcoin">
    <meta property="og:article:tag" content="Bitcoin Cash">
    <meta property="og:article:tag" content="BCH">
    <meta property="og:article:tag" content="Cryptocurrency">
    <meta property="og:article:tag" content="BTC">
    
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://minisatoshi.cash">
    <meta name="twitter:site" content="@_minisatoshi">
    <meta name="twitter:creator" content="@_minisatoshi">
    <meta property="twitter:title" content="What is Bitcoin Cash (BCH)? | The Freedom Money Revolution">
    <meta property="twitter:description" content="Discover Bitcoin Cash (BCH): a fast, low-cost, decentralized cryptocurrency designed for everyone. Join the freedom revolution! | minisatoshi.cash">
    <meta property="twitter:image" content="https://minisatoshi.cash/images/minisatoshicash.jpg?v=2">
    
    <!-- Meta Tags Generated with https://metatags.io -->
    <meta name="keywords" content="Bitcoin, Bitcoin Cash, BTC, BCH, Satoshi, Bcash, crypto, digital currency, crypto news, DeFi, altcoin, what is bitcoin cash">
	<meta name="robots" content="index, follow, max-image-preview:large">
    <meta name="language" content="English">
    <meta name="revisit-after" content="7 days">
    <meta name="author" content="_minisatoshi">
```

The above samples what OG and Twitter and SE cards would be like. The Twitter is probably the most important. The main detail here is the "content="summary_large_image"" argument. This will provide a large card image with the description below. For large images, 800px by 418px is the recommended resolution (.jpg (transparency doesn't work great)). You can also do a "summary" instead if you want a smaller square (recommended resolution of 400x400px) image with the description on the right of the smaller image.

However, adding this code is NOT ENOUGH alone (not always). You need to use these tools:
For Twitter/X: Sometimes X will pick up new cards by itself, but other times it will not. The best way to ensure it does is to visit this site and provide the URL for each site/page that has a card: https://cards-dev.twitter.com/validator
The validator has largely been deprecated so you can't see the preview on that page, but it still will force X to refresh any card previews it generates, along with tags and more.
As for Telegram, you MUST send the URLs to this bot: @WebpageBot
Each website/page needs a URL to be sent. Below is an image showing the options and the difference between a site with a card set in HTML and a site without:
You'll notice options to Update Preview and Update Content, press both buttons after sending a URL. Then you're good to go! The below site does not have a card (yet) so when sending a link nothing happens. This is how they will appear in chats!
![Screenshot 2025-04-29 at 13.33.36|690x424](upload://loK5thqbALriyN0mafqXE7KZcny.jpeg)


***Existing Media Article Enhancements***

Submitting requests to different sites that write articles about Bitcoin Cash or "What is BCH" and asking for them to be updated with sources can be helpful. For instance, this is what I recently sent to Investopedia:

'''
Hello!

Overall I think you got a great start to a BCH article. Nowadays, it is a bit out of date and there have been some massive developments which could be worth including.

In short, I would recommend checking out some sites such as https://whatisbitcoin.cash and https://discover.cash for high level overviews of updates, see a few bullets below (more info can be found on these sites!):

- BCH has massively upgraded scripting enabling robust contracts in comparison to ethereum and Solana -- the main upgrade enabling this was CashTokens in 2023 (https://minisatoshi.cash/upgrade-history#upgrade-CashTokens), but many others have also worked to improve this

- This also means BCH has DEXs such as Cauldron.Quest and TapSwap.cash with FT and NFT trading, all while leveraging the benefits of UTXOs

- DeFi has greatly expanded too. For some quick details, there's a great post here: https://bchbull.com/blog/is-defi-ready-for-bch

- BCHBull is one of the largest DeFi applications with over 500,000BCH in platform volume - it enables permission less, on-chain leverage and hedge trading against a number of currencies, cryptos, and commodities

- The ecosystem has massively expanded: https://minisatoshi.cash/ecosystem

- BCH has privacy tools such as CashFusion and RPA -- CashFusion has had massive volume with over 27 million BCH fused since 2019 (https://fusionstats.redteam.cash)

The above bullets are meant to stay pretty high level with some cherrypicked neat examples, but I hope the editors can take a quick peek and add some newer information!
'''

Will anything happen? Can't know unless we try. But I assure you most other smaller cryptos are NOT doing this, and we have a passionate enough community to really make a difference to anyone else looking in from the outside. And this could even lead to new article creation... particularly if we think about neat tools like BCHBull and CashTokens.


***New Media/Article Requests***

Not much more to share, but apply the same idea from right above to this. Many sites have places to suggest new articles. Can even give draft articles. Linking to new developments, tool releases, and blog posts could be very beneficial. All it takes is one or two sources to pick up a story.


***Broader Image/Graphic Sharing***
If you create graphics, memes, stickers, etc related to BCH, or take photos of merchants with BCH stickers or of you spending BCH, post it! And not just on social media, post it on places like Wikimedia! Below see a screenshot of what a post would look like. Tagging Bitcoin Cash and otherwise and putting it in the image description helps a lot, and will get more attention as people search for images. These will also appear very high in Google Images and Bing Images rankings.
![Screenshot 2025-04-29 at 12.53.26|441x500](upload://ekxL5ApI8a43rdBuleoG0etKPau.png)





----------------------------------------------------------------------------------------
<head> Tag Sample
----------------------------------------------------------------------------------------

```
	<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
    <meta name="format-detection" content="telephone=no">
    <!--Prevents browsers from trying to make a number a clickable phone number (can still use "tel:" if we want this functionality)-->
    
    <!-- Favicon + Web App -->
	<link rel="icon" type="image/png" href="/favicon/favicon-96x96.png" sizes="96x96">
	<link rel="icon" type="image/svg+xml" href="/favicon/favicon.svg">
	<link rel="shortcut icon" href="/favicon/favicon.ico">
	<meta name="mobile-web-app-capable" content="yes">
	<link rel="apple-touch-icon" sizes="180x180" href="/favicon/apple-touch-icon.png">
	<meta name="apple-mobile-web-app-title" content="minisatoshi">
	<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
	<link rel="manifest" href="/favicon/site.webmanifest">
	<meta name="msapplication-TileImage" content="/favicon/favicon-96x96.png">
    
    <!-- Canonical link for SEO -->
    <link href="https://minisatoshi.cash" rel="canonical" data-rh="true">
    <link href="https://minisatoshi.cash" hreflang="x-default" rel="alternate" data-rh="true">
    
    <!-- Primary Meta Tags -->
    <title>What is Bitcoin Cash? | The Freedom Money Revolution</title>
    <meta name="title" content="What is Bitcoin Cash (BCH)? | The Freedom Money Revolution">
    <meta name="description" content="Discover Bitcoin Cash (BCH): a fast, low-cost, decentralized cryptocurrency designed for everyone. Join the freedom revolution! | minisatoshi.cash">
    
    <!-- Use Google Search Console and Bing Webmaster Tools for SEO data -->
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://minisatoshi.cash">
    <meta property="og:title" content="What is Bitcoin Cash (BCH)? | The Freedom Money Revolution">
    <meta property="og:description" content="Discover Bitcoin Cash (BCH): a fast, low-cost, decentralized cryptocurrency designed for everyone. Join the freedom revolution! | minisatoshi.cash">
    <meta property="og:image" content="https://minisatoshi.cash/images/minisatoshicash.jpg?v=2">
    <meta property="og:image:alt" content="minisatoshi.cash homepage image.">
    <meta property="og:article:section" content="Information">
    <meta property="og:article:tag" content="Bitcoin">
    <meta property="og:article:tag" content="Bitcoin Cash">
    <meta property="og:article:tag" content="BCH">
    <meta property="og:article:tag" content="Cryptocurrency">
    <meta property="og:article:tag" content="BTC">
    
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://minisatoshi.cash">
    <meta name="twitter:site" content="@_minisatoshi">
    <meta name="twitter:creator" content="@_minisatoshi">
    <meta property="twitter:title" content="What is Bitcoin Cash (BCH)? | The Freedom Money Revolution">
    <meta property="twitter:description" content="Discover Bitcoin Cash (BCH): a fast, low-cost, decentralized cryptocurrency designed for everyone. Join the freedom revolution! | minisatoshi.cash">
    <meta property="twitter:image" content="https://minisatoshi.cash/images/minisatoshicash.jpg?v=2">
    
    <!-- Meta Tags Generated with https://metatags.io -->
    <meta name="keywords" content="Bitcoin, Bitcoin Cash, BTC, BCH, Satoshi, Bcash, crypto, digital currency, crypto news, DeFi, altcoin, what is bitcoin cash">
	<meta name="robots" content="index, follow, max-image-preview:large">
    <meta name="language" content="English">
    <meta name="revisit-after" content="7 days">
    <meta name="author" content="_minisatoshi">
    
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&amp;display=swap" rel="stylesheet" type="text/css" media="all">
    
    <!-- Bootstrap and Dependencies -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous" defer></script>

    <!-- ParticlesJS -->
	<script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>

  	<!-- Custom JS -->
    <script src="js/particles-toggle.js?v=2" defer></script>
    
    <!-- Dynamically loading main.css and themeInit.js -->
    <script>
        console.log("Dynamic script block running");
        const version = Date.now();
        console.log("Version:", version);

        const cssLink = document.createElement('link');
        cssLink.rel = 'stylesheet';
        cssLink.href = `/css/main.css?v=${version}`;
        cssLink.onload = () => console.log("main.css loaded");
        cssLink.onerror = (e) => console.error("main.css failed to load:", e);
        document.head.appendChild(cssLink);

        const themeScript = document.createElement('script');
        themeScript.src = `/js/themeInit.js?v=${version}`;
        themeScript.onload = () => console.log("themeInit.js loaded");
        themeScript.onerror = (e) => console.error("themeInit.js failed to load:", e);
        document.head.appendChild(themeScript);

        const particleConfig = document.createElement('script');
        particleConfig.src = `/js/particles-config.js?v=${version}`;
        particleConfig.onload = () => console.log("particles-config.js loaded");
        particleConfig.onerror = (e) => console.error("particles-config failed to load:", e);
        document.head.appendChild(particleConfig);
    </script>

    <!-- Schema -->
    <script type="application/ld+json">
	{
	  "@context": "https://schema.org",
	  "@type": "WebPage",
	  "name": "What is Bitcoin Cash? | MiniSatoshi",
	  "description": "Learn about Bitcoin Cash (BCH), a peer-to-peer electronic cash system."
	},
	{
	  "@context": "https://schema.org",
	  "@type": "FAQPage",
	  "mainEntity": [
	    {
	      "@type": "Question",
	      "name": "What is Bitcoin Cash?",
	      "acceptedAnswer": {
	        "@type": "Answer",
	        "text": "Bitcoin Cash (BCH) is a fast, low-cost, decentralized cryptocurrency designed for everyone."
	      }
	    }
	  ]
	}
    </script>

    <!-- Add theme-color meta tag -->
    <meta name="theme-color" id="themeColorMeta">
	</head>
```
