title:: Introducing Tailnet Lock: Use Tailscale Without Trusting Our Infrastructure! (highlights)
author:: [[tailscale.com]]
full-title:: "Introducing Tailnet Lock: Use Tailscale Without Trusting Our Infrastructure!"
category:: #articles
url:: https://tailscale.com/blog/tailnet-lock/

- Highlights first synced by [[Readwise]] [[Dec 17th, 2022]]
	- Users sometimes ask us, “How can I trust Tailscale?” From the beginning, we’ve tried to make it so you don’t have to, by architecting our infrastructure with security and privacy in mind. When you use Tailscale, your data is end-to-end encrypted. Tailscale doesn’t have the private key, so we can’t see your traffic. While Tailscale can’t observe the data transiting your tailnet, we are responsible for managing the control plane, where our coordination server distributes public keys and settings for your tailnet.
	  Which brings us to one glaring issue that has remained with our architecture: You have still needed to trust our coordination server. What if we were malicious, and stealthily inserted new nodes into your network? Tailscale could hypothetically use a secretly-added node to send or receive traffic to your existing nodes — meaning it wouldn’t matter that the traffic is encrypted because the peer itself would be malicious.