<script>
    import GTag from "./GTag.svelte";
    import favicon from "../../assets/favicon.ico";
    import fbImage from "../../assets/media/logo.png";
    let meta = {
        name: "Ansel Kipchumba Melly",
        title: "Ansel Melly - Software and Web Applications Consultant",
        description:
            "Ansel Melly: software and web applications consultant with speciality in simple,complex and custom applications.Specializes in PHP,Laravel,Wordpress,Symphony, Javascript, HTML, CSS, Mysql, Linux server administration",
        image: fbImage,
        url: "https://anselmelly.com",
    };
</script>

<svelte:head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta
        name="google-site-verification"
        content="w1gewQK3moI5ZcbPmKPglTV6VV6jpXXs_F0_d65xeTU"
    />
    <meta name="Description" content={meta.description} />
    <title>{meta.title}</title>
    <link rel="icon" href={favicon} />
    <meta name="author" content={meta.name} />
    <meta property="og:url" content={meta.url} />
    <meta property="og:type" content="website" />
    <meta property="og:title" content={meta.title} />
    <meta property="og:description" content={meta.description} />
    <meta property="og:image" content={fbImage} />
    <GTag />
    <script
        async
        defer
        crossorigin="anonymous"
        src="https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v12.0&appId=236996503126712&autoLogAppEvents=1"
        nonce="AFE6UtAq"></script>
    <link rel="me" href="https://twitter.com/ansymelly" />
   

<script>window.twttr = (function(d, s, id) {
    var js, fjs = d.getElementsByTagName(s)[0],
      t = window.twttr || {};
    if (d.getElementById(id)) return t;
    js = d.createElement(s);
    js.id = id;
    js.src = "https://platform.twitter.com/widgets.js";
    fjs.parentNode.insertBefore(js, fjs);
  
    t._e = [];
    t.ready = function(f) {
      t._e.push(f);
    };
  
    return t;
  }(document, "script", "twitter-wjs"));</script>


</svelte:head>
