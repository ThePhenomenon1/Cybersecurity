# Firewall
Fighting SQL injections and other broad surface exploits.


The past few days I've been under attack from bots. Nothing spectacular - just trying SQL injections and other broad surface exploits. I was able to catch them due to some bugs in my forms and got alerts from Sentry as a result.

I'm using Cloudflare and was surprised that the attacks weren't mitigated. I then realized that I've done something really stupid - I'd simply forgotten to set up my server firewall to only allow traffic from Cloudflare's IPs. This means that all the bots were probing my server directly, circumventing Cloudflare.

Once I remedied that, traffic and server load dropped dramatically.

As an extra layer of security, I also wrote a small middleware which blocks the IP once they've accrued a certain amount of 400 status responses in a specific timeframe.

Credit: Denisbotev
