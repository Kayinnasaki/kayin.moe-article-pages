---
process:
    markdown: true
    twig: true
title: 'Site Map'
cache_enable: false
nodate: '1'
---
<style type="text/css" media="screen">

a:link { color: #436fa8;}
a:visited { color: #436fa8; }
a:hover { color: var(--color-link); }

[data-theme="dark"] {
    a:link { color: var(--color-text);}
    a:visited { color: var(--color-text); }
    a:hover { color: var(--color-link); }
}

</style>
### Feeds

**[RSS Feed](/writing.rss) : [ATOM Feed](/writing.atom) : [JSON Feed](/writing.json)**

### List of Post Tags

{% include 'partials/taxonomylist.html.twig' with {base_url: my_url, taxtype: 'tag'} %}

### List of Games Mentioned
<div markdown=1 class="flextags">
{% include 'partials/taxonomylist.html.twig' with {base_url: '', taxtype: 'games', listtype: 'full' } %}
</div>
</div>