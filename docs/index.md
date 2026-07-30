# ME204 Final Project

# Two countries tax sugary drinks. Only one of them has less sugar.

Sugar taxes are spreading across Europe on a simple theory: make sweeter drinks
more expensive to sell, and manufacturers will reformulate them. It is a claim you
can check without any policy modelling at all — just look at what is actually on
the shelves.

So I did. Every soft drink listed in Open Food Facts, a public food database, for
four European markets. **6,086 drinks with a recorded sugar content.**

<span style="color:#3995ba"><strong>The United Kingdom and France</strong></span>
tax sugary soft drinks.
<span style="color:#c63c4a"><strong>Germany and Italy</strong></span> do not —
Italy passed a sugar tax in 2019, but it has been postponed so many times it has
never actually come into force.

---

## The obvious comparison finds nothing at all

Put the two taxed countries in one group and the two untaxed ones in another, and
the difference is 0.06 g of sugar per 100g. Nothing. On that number alone you
would conclude sugar taxes do not work.

That comparison is broken, though, and it is worth seeing why. The database holds
far more French products than any other — France alone makes up 89% of the "taxed"
group, and Germany 85% of the "untaxed" one. France and Germany happen to be very
similar. So the pooled figure is really just France against Germany, with
everything else drowned out.

Look at the four countries separately and the picture changes completely.

---

## Britain is the exception

## 4.60 g vs 10.00 g
Sugar in the typical full-sugar soda, United Kingdom against Italy

![Sugar content by country](docs/sugar_by_country.png)

The typical Italian soft drink contains **more than twice** the sugar of the
typical British one. Germany and France sit in between, closer to Italy than to
Britain.

Crucially, these are the drinks that still contain sugar — every zero-sugar
product has already been taken out. That matters, because there is an obvious
objection to any comparison of averages: maybe Britain is not making sweeter
drinks less sweet, maybe it is just selling more diet versions alongside the
unchanged originals.

It is doing both.

![Share of sodas with no sugar](docs/diet_by_country.png)

> A quarter of British sodas contain no sugar at all — more than any other
> country here. And the ones that *do* contain sugar have markedly less of it.
> Both at once is what reformulation looks like.

---

## France has the same policy and none of the result

Here is the part that does not fit.

France has taxed sugary drinks since 2012, and restructured the tax in 2018 so
that the rate rises with sugar content. If a sugar tax reliably drives
reformulation, France should look like Britain.

It does not. French sodas contain **more** sugar than German ones — 8.22 g against
7.68 g per 100g — despite Germany having no tax at all. France also carries a
smaller share of zero-sugar drinks than untaxed Italy.

Two countries, the same policy, opposite outcomes. Whatever makes Britain
different, it is not simply the existence of a sugar tax. It might be how the levy
was designed, or when it was announced, or something about the British market that
has nothing to do with tax at all. This data cannot say which — but it can say
that "countries with sugar taxes have less sugary drinks" is not true as a general
rule.

---

## What this does not show

This is a photograph, not a film. It shows what is on the shelves now, not what
was there before each policy arrived. Britain having lower-sugar drinks today is
consistent with the levy having caused it — but a country could have got there for
reasons that have nothing to do with tax, and nothing here rules that out.

The database is also built by volunteers, so how thoroughly each market has been
catalogued varies a great deal. That is worth holding in mind alongside every
figure above.

---

*Data: [Open Food Facts](https://world.openfoodfacts.org) — every soda listed for
the four countries, 6,557 products, of which 6,086 record a sugar value. Collected
July 2026. Full method, code and limitations:
[GitHub repository](https://github.com/JaviMilagro/me204-final-project).*


- https://github.com/JaviMilagro/me204-final-project/blob/main/README.md 

