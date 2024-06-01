# Firewall
Fighting SQL injections and other broad surface exploits.


When under attack from bots: facing SQL injections and other broad surface exploits. You can catch them utilizing alerts from Sentry.

Using Cloudflare, you forget to set up your server firewall to only allow traffic from Cloudflare's IPs. This means that all the bots probe the server directly, circumventing Cloudflare.

Once this is remedied, traffic and server load will drop dramatically.

As an extra layer of security, here's a coded middleware which blocks the IP once they've accrued a certain amount of 400 status responses in a specific timeframe.

Credit: Denisbotev
