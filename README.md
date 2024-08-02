# Firewall
Fighting SQL injections and other broad surface exploits.


When under attack from bots and you are facing SQL injections and other broad surface exploits: you can intercept them utilizing alerts from Sentry. (Sentry is an application performance monitoring and error-tracking software.)

However, what if while using Cloudflare, you forget to set up your server firewall to only allow traffic from Cloudflare's IPs? This means that all the bots probe the server directly, circumventing Cloudflare.

Once this oversight is remedied, traffic and server load will drop dramatically.

As an extra layer of security, here's a coded middleware (Middle Firewall file) which blocks the IP once they've accrued a certain amount of 400 status responses in a specific timeframe.

Credit: Denisbotev
