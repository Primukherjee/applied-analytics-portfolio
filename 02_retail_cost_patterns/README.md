TITLE: Hidden Revenue Dependency Patterns in Retail Data;

What I’m Curious About;

When we look at revenue, we usually look at totals. Growth. Maybe trends over time.

But what if the structure underneath tells a different story?

More specifically:

Is revenue concentrated in just a few regions?

Do a handful of customers carry most of the business?

Are there signals of instability hidden in transaction patterns?

What happens if one major customer disappears?

This isn’t about predicting failure. It’s about noticing where systems might be fragile without realizing it.;

Why This Matters to Me;

In psychology, we’re trained to treat patterns as early warnings. If behavior starts clustering in strange ways, something underneath is shifting. Businesses aren’t that different.

If most revenue comes from a small set of customers or locations, that creates quiet dependency. Everything looks stable. Until it isn’t.

Lose one region. Lose one large client. Suddenly things change fast.

I wanted to look at revenue not as a single number, but as a structure. Something with pressure points. Something that could bend.;

The Data;

For this project, I used a publicly available online retail dataset from Kaggle. It contains transaction-level information — product purchases, quantities, prices, timestamps, customer IDs, and country information.

I’m treating it as illustrative, not definitive. It’s a snapshot of real purchasing behavior. That’s enough to study patterns.

What matters here isn’t the specific company. It’s the structure that shows up when you step back and look at how revenue actually forms.;

How I Approached the Analysis;

I kept things simple and readable. No heavy modeling. No black boxes. Just patterns.

I used Python and SQLite together to work with the data in a way that felt closer to real business workflows. Loaded the dataset. Queried it. Aggregated it. Looked at how revenue spreads across countries, customers, and time.

Some of the things I explored:

Revenue distribution across countries;
Customer concentration — who generates most of the income;
Average order value vs frequency of purchases;
Monthly revenue movement over time;
Signals of dependency where a small segment drives a large share of revenue;

I wasn’t trying to build a prediction engine. I wanted to understand structure.;

What Stood Out;

A few things became obvious pretty quickly.

Revenue wasn’t evenly distributed. Not even close.

Certain countries dominated, with one region contributing a disproportionate share of total income.

A small group of customers generated a large portion of revenue. Some bought frequently in smaller amounts. Others made fewer but much larger purchases. Different patterns, same impact.

Monthly revenue wasn’t steady either. It rose and fell across time, showing that income flow isn’t constant.

Taken together, it pointed toward concentration.

If a business depends heavily on a few places or a few customers, that creates exposure. Not immediate danger. But structural vulnerability.;

Why I Think This Kind of Analysis Matters;

We talk a lot about growth. Revenue going up. Numbers looking good.

But concentration matters too.

If income comes from everywhere, that’s resilience.
If it comes from just a few pockets, that’s exposure.

This kind of analysis doesn’t give answers. It just points at pressure points.

And sometimes that’s enough.;

Key Takeaways;

Revenue is heavily concentrated in a small number of countries;
A limited group of customers generates a large share of total income;
Some customers drive revenue through frequent purchases, others through high-value orders;
Monthly revenue fluctuates, suggesting uneven demand over time;
Business stability may depend more on structure than total revenue size;
Looking at patterns beneath the totals reveals hidden dependencies;

Limitations;

This is exploratory work using one dataset. That means a few things:

I can’t make causal claims;
The business context is missing;
Customer behavior here might not reflect other industries;
Some fields have missing values;

So I treat this as pattern-spotting, not truth-finding.

The goal is to practice thinking in systems. Looking at data as something connected, not isolated.;

Tools Used;

Python (pandas, matplotlib);
SQLite (query-driven analysis);
Jupyter Notebook;

What I Found / Interpretation

Written in your voice. Bullet-pointed. Conversational. Based directly on the analysis you ran.

What I Found

Instead of looking at revenue as one big number, I tried to break it apart and see where it was actually coming from. A few patterns stood out almost immediately.

Geographic concentration

Revenue is heavily concentrated in a small number of countries.

The United Kingdom alone contributes a disproportionately large share compared to the rest.

After the top few countries, there’s a steep drop-off.

This suggests the business isn’t evenly distributed globally — it leans heavily on certain regions.

What that means:
If demand drops in one major region, total revenue could take a noticeable hit. It’s not just about performance. It’s about exposure.

Customer concentration

A relatively small number of customers generate a large portion of the total revenue.

Some customers show extremely high transaction counts, meaning they purchase frequently.

Others buy rarely but place very large orders when they do.

What that means:
Revenue isn’t being driven equally by everyone. It’s coming from a core group. That creates dependency. If even a few of those customers leave, the impact could be significant.

Frequency vs spending behavior

Some top customers generate revenue through volume — lots of purchases over time.

Others contribute through high-value orders despite fewer transactions.

Both patterns matter, but they represent different types of customer relationships.

What that means:
Loyalty and purchasing power show up in different ways. One customer might be consistent. Another might be occasional but big. Losing either type would hurt, just in different ways.

Revenue inequality

When I calculated approximate total revenue, it became clear that income isn’t spread evenly across the dataset.

A small segment appears to drive a large chunk of financial activity.

This kind of imbalance is common in real-world businesses.

What that means:
The business may look stable on the surface, but structurally it’s leaning on a few strong pillars.

Time-based trend

Monthly revenue fluctuates rather than growing steadily.

There are clear peaks and dips across the year.

Some months show strong surges, followed by noticeable drops.

What that means:
Revenue flow isn’t consistent. It’s seasonal or event-driven. That kind of volatility can make planning harder.

Returns signal (unexpected finding)

After cleaning the data to remove negative quantities, return signals disappeared from the analysis.

That suggests either:

Returns were filtered out during cleaning, or

Returns exist but are limited in this processed version.

What that means:
This part of the analysis became less informative than expected, but it still showed how preprocessing decisions can shape what we’re able to detect.

Bigger Picture Insight

Taken together, the patterns point toward structural concentration.

Revenue seems to depend heavily on:

A few countries

A few high-value customers

Specific time periods

None of this is inherently bad. But it does mean the system might be sensitive to change. If one major segment weakens, the effect could ripple through everything else.

That’s the part I found most interesting — not the total revenue itself, but where it actually comes from.
