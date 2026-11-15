# DMIT Corona: What the $49.9/Year LAX EB Plan Includes, Who the CMIN2 + 9929 Return Route Suits, and When WEE or FONTANA Is the Better Buy (Full Plan Table)

DMIT Corona is the **$49.9**/year annual plan in DMIT's Los Angeles Eyeball (LAX EB) line, and it ships with 1 vCore, 1GB of RAM, 20GB of NVMe storage, **2TB** of bidirectional monthly transfer and a **2Gbps** port. China Unicom and China Mobile users get the most out of it because both directions of their traffic ride premium routes. Telecom users who need a flat peak-hour curve should price the Pro series before paying.

Below is what the plan actually routes, how it differs from the cheaper WEE and the larger FONTANA, what a year really costs, and which policy pages to read before checkout.

> **Short answer:** if you need 2TB a month and a 2Gbps port on an optimized US west coast route, CORONA at **$49.9**/year is the tier to buy. Under 1TB a month, take WEE and save $10. If 2 vCores or 2GB of RAM is the real constraint, jump to FONTANA.
> 👉 [See the current LAX EB plan list and stock status](https://www.dmit.io/aff.php?aff=9081)

## The full LAX EB lineup

| Plan | vCPU / RAM | Storage | Transfer / Port | Price | Order |
| --- | --- | --- | --- | --- | --- |
| LAX.EB.WEE | 1 / 1GB | 20GB | 1TB / 1Gbps | $39.9/year | [ Order WEE](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.CORONA | 1 / 1GB | 20GB | 2TB / 2Gbps | $49.9/year | [ Order CORONA](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.FONTANA | 2 / 2GB | 40GB | 4TB / 4Gbps | $100/year | [ Order FONTANA](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.TINY | 1 / 2GB | 20GB | 1.5TB / 2Gbps | $12.98/month | [ Order TINY](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.Pocket | 2 / 2GB | 40GB | 3TB / 4Gbps | $18.90/month | [ Order Pocket](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.STARTER | 2 / 2GB | 80GB | 5TB / 4Gbps | $38.90/month | [ Order STARTER](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.MINI | 4 / 4GB | 80GB | 10TB / 10Gbps | $76.90/month | [ Order MINI](https://www.dmit.io/aff.php?aff=9081) |
| LAX.EB.MICRO | 4 / 4GB | 160GB | 14TB / 10Gbps | $99.90/month | [ Order MICRO](https://www.dmit.io/aff.php?aff=9081) |

All plans are KVM with one IPv4 plus a /64 IPv6 block, and transfer is billed in both directions (upload plus download counts against the quota, which is why 2TB on paper is less than 2TB of downloads). The three annual tiers are stable across every source checked for this article. Monthly tier names, core counts and prices move with the hardware batch in rotation (AN4 versus AN5), so treat the monthly rows as a shape rather than a fixed price and confirm on the order page.

## How CORONA's route actually runs

Two directions, two different carrier sets, and only one of them is what you're paying the premium for.

**Outbound, China to Los Angeles:** Telecom and Unicom hand off on CN2. Mobile goes out on CMIN2.

**Return, Los Angeles to China:** Telecom returns on CMIN2, with 9929 used for load balancing in some conditions. Unicom returns on AS9929. Mobile returns on CMIN2.

The return leg is where most of the felt experience lives. Downloading a file, loading a page, watching a stream: the packets that matter to you travel VPS to China, which is exactly the path that ordinary transit providers let degrade at 8pm. EB buys an optimized return and pairs it with a CN2 outbound for Telecom and Unicom.

EB is not CN2 GIA. Listings that describe the return route as "three-network CN2 GIA" are describing the Pro line, and the price difference between the two lines exists for that reason.

What each operator gets:

**Unicom.** CN2 out, 9929 back. This is the combination that shows up as the most consistent in third-party traces, with reported latency of 130–160ms from mainland nodes and the smallest swing during the evening peak.

**Mobile.** CMIN2 in both directions, so the whole path stays on China Mobile's own international product. Reported latency of 125–155ms is the lowest of the three, and the double-ended optimization is why Mobile users often report this plan performing above its price.

**Telecom.** CN2 outbound is a genuine step up from plain transit, but the return lands on CMIN2 or 9929 rather than Telecom's own GIA. Reported latency sits at 140–170ms. If your work tolerates that, CORONA is fine. If a spike at 9pm breaks something, the Pro series is the answer and the extra money is buying the return path, not the hardware.

Test IP for your own checks before buying: 154.17.226.2. Ping it from the connection you'll actually use, at the hour you'll actually use it.

## CORONA vs WEE vs FONTANA vs Pro

**WEE, $39.9/year.** Identical route to CORONA. Same carriers, same optimization, same 1 vCore and 1GB. The $10 gap buys transfer volume and port speed only: 1TB and 1Gbps versus 2TB and 2Gbps. Anyone whose monthly traffic stays under 1TB should take WEE and stop reading.

**CORONA, $49.9/year.** The tier to pick when you expect to move somewhere between 1TB and 2TB a month, or when the 2Gbps port matters for burst transfers. A small site, a household proxy, a bot, or a relay between two services all fit comfortably.

**FONTANA, $100/year.** Doubles everything CORONA has: 2 vCores, 2GB of RAM, 40GB of storage, 4TB and 4Gbps. Buy this when RAM is the binding constraint (a database, a couple of containers, a build runner), not when traffic is.

**Pro series.** Three-network CN2 GIA in both directions, less transfer for more money. Correct for Telecom users with latency-sensitive traffic, and for anyone who needs the peak hour to be uneventful.

## What a year actually costs

$49.9 spread over 12 months is $4.16 per month. That covers the 2TB, the 2Gbps port and the optimized return path, and on this tier the annual price is also the renewal price unless DMIT changes list pricing.

A discount code circulates in third-party writeups: `LAX-EB-LAUNCH-NON-MONTHLY-RECURRING-20OFF`, described as a recurring 20% off for quarterly and longer billing, applied again on renewal rather than once. It could not be confirmed on DMIT's own pricing page while preparing this article. Type it into the promo field at checkout and read the line total before paying. Twenty percent off $49.9 works out to just under $40 a year, and a code that doesn't apply simply leaves you at $49.9. Don't choose a billing cycle on the assumption the code works.

👉 [Check the CORONA price on the DMIT order page](https://www.dmit.io/aff.php?aff=9081)

## The policies worth reading before you pay

Three things come up in every discussion of this plan, and the sources disagree on the specifics. That's an argument for reading the terms attached to the plan at checkout, not an argument for skipping them.

**Over-quota traffic.** The plan throttles rather than suspends. Past 2TB, the port drops to a low fixed rate and the server keeps running, which means SSH and light traffic still work. Published throttle figures differ between writeups (2 Mbps in one, 4 Mbps in another, for the same plan), so treat the exact number as something to verify rather than a spec.

**IP replacement.** One description requires 7 days since purchase, 15 days since the last swap, and a genuinely blocked IP before a free replacement; another says a free swap every 15 days, blocked or not. For mainland use this is the policy that matters most, because IP blocks are a routine event rather than an emergency, and the difference between those two versions decides whether a bad week costs you $5.

**Refunds.** Descriptions range from a 3-day window with a 30GB usage cap up to a 30-day pro-rata refund. The window and its conditions determine whether a disappointing first week is recoverable, and they're stated on the order page.

Payment options include credit card, PayPal and cryptocurrency (USDC, USDP and USDG across Ethereum, Polygon and Base). Some writeups also list Alipay and WeChat Pay; if that's how you want to pay, confirm it at checkout rather than assuming.

👉 [Open the LAX EB order page and read the current terms](https://www.dmit.io/aff.php?aff=9081)

## Hardware, benchmarks, and where the numbers come from

DMIT runs two hardware generations in Los Angeles. AN4 is built on AMD EPYC 9654 (9004 series). AN5 moves to EPYC 9005 "Turin" with a higher single-core score. Current listings are mostly AN5, and AN4 machines from earlier batches are still in customers' hands, so which one you receive depends on the batch attached to the plan when you order. The order page shows it.

Everything below is from third-party tests and community records, not from a machine run for this article:

- Latency from mainland China: roughly 125–155ms on Mobile, 130–160ms on Unicom, 140–170ms on Telecom.
- Throughput: 725 Mbps down on Shanghai Unicom and 747 Mbps up on Suzhou Telecom in published tests, with iperf3 uplinks regularly in the hundreds of Mbps.
- Disk: fio 64k sequential reads and writes both above 1 GB/s, so storage isn't the bottleneck for a small site or a database.
- Streaming: native US IP with Netflix and ChatGPT generally working. IP databases classify the address as datacenter/hosting, and platform rules change without notice, so no seller can promise that holds.

## Who should skip CORONA

- **Anyone under 1TB a month.** WEE is the same server on the same route for $10 less.
- **Telecom users who need a flat evening curve.** CN2 out plus CMIN2/9929 back is good; three-network CN2 GIA is better, and that's Pro.
- **Anyone who needs more than 1GB of RAM.** Container stacks, JVM apps and busy databases hit the ceiling quickly. FONTANA doubles RAM, cores, storage and transfer for $100/year.
- **Buyers who need Hong Kong or Tokyo latency.** This is a Los Angeles box. The 125–170ms range is the floor, not a temporary condition caused by congestion.

## Picking one

Traffic under 1TB and 1 vCore is enough: WEE. Somewhere between 1TB and 2TB, or you want the 2Gbps port: CORONA. Two cores, 2GB of RAM or 2–4TB of transfer: FONTANA. Telecom with latency-sensitive traffic: Pro, and budget accordingly.

Two things to confirm at checkout before the card comes out. First, the actual line total and billing cycle, including whether the promo code applied and what the renewal price will be. Second, the refund and IP replacement terms attached to that specific plan, since those decide how much a bad first month costs you.

👉 [Go to the DMIT LAX EB order page and pick the plan](https://www.dmit.io/aff.php?aff=9081)
