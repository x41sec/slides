---
published: true
title: Shadow on the Wall - Risks and Flaws with Shadowsocks
layout: advisory
categories: [news, security]
tags: news
author: Niklas Abel
date: 2018-07-05
excerpt: X41 shows several vulnerabilities and design issues with Shadowsocks and its tools
---

## About the Talk

What is one of the cornerstones of the Internet? Right! Being able to access all kinds of information, without censorship. In some countries this is no longer possible, and this is why technologies such as Tor and Shadowsocks are needed.

While the main feature of Tor is the onion routing and the aim of being cryptographically secure, it can easily be blocked by a firewall.

Shadowsocks simply tries to provide an undetectable tunnel to a non-censored part of the Internet.

Shadowsocks provides a Socks5proxy locally, into which all traffic is routed. It encrypts traffic with a configurable symmetric algorithm and the messages have (pseudo) random lengths. The absence of any visible protocol information makes them appear totally random. The goal is stealth through restricted infrastructures.

Naturally, users of such tools may be exposed to increased risks. Therefore the tools aim to be undetectable by deep packet inspection firewalls. For security and privacy they have to encrypt the traffic, use random padding, ensure integrity, and should imitate other protocols so as to look like normal encrypted traffic, e.g. such as that from an encrypted website. The server should be authenticated to ensure that the user does not communicate with a malicious endpoint.

We had a look at Shadowsocks to see how it handles this task, and noticed some interesting things.

This talk shows the results of our efforts to analyse ShadowSocks and identifying real vulnerabilities. There were [attempts](https://github.com/madeye/sssniff) about detecting shadowsocks. We [show](https://github.com/x41sec/slides/raw/master/2018-passthesalt/shadowsocks_slides_pass_the_salt_2018.pdf) how to brute force it, manipulate its log files. In addition, we show several local as well as remote command execution vulnerabilities affecting shadowsocks and its tools.

## Get in touch!

If you have questions about advanced attacks, security audits, or other security research, please [get in touch](https://www.x41-dsec.de/#contact) with us.
