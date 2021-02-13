---
layout: post
comments: true
title: The very first release of p-winds
author: Leo dos Santos
permalink: /blog/:year/:month/:day/:title:output_ext
tag: 2021
excerpt_separator: <!--more-->
---

Today's post is going to get a bit technical on the physics and astronomy side, so buckle up for it because we are talking about scientific software! I have just made the alpha release of [`p-winds`](https://p-winds.readthedocs.io), my very first take into modelling planetary atmospheres. And I am particularly proud of this one, because: 1) the code is fully open source and thoroughly documented, and 2) I believe this project can potentially be useful to many other astronomers like me that observe exoplanetary atmospheres.

<!--more-->
{:refdef: style="text-align: center;"}
![Mars](/blog_assets/2021-02-07.JPG "Mars?")
{: refdef}

But first let me give you a little bit of background. You see, the questions that scientists ask themselves can sometimes be kind of silly, but they may turn out to be quite a predicament to answer. Back in the late 19th Century, with the development of kinetic theory for gases, which describes the random motion of gas molecules, some scientists started putting two and two together: "Wait, if the gas in our atmosphere does indeed move about randomly, the molecules can eventually escape to space. Does that mean our atmosphere could slowly evaporate with time?" \[[^1]\]. Well, turns out those silly people were onto something here.

Nowadays, with the discovery of thousands of exoplanets, atmospheric escape and evaporation is considered one of the most important physical processes surrounding the evolution of their atmospheres \[[^2]\]. But things can get a bit complicated from here, because in order to describe the physics behind atmospheric escape, we need to deal with some really pesky differential equations. However, there is one very famous mathematical simplification that is frequently used to model stellar and planetary outflows: it is called the *Parker wind model* \[[^3]\]. I won't get into the details of this model here, but suffice to say that it saves us a lot of time and frustration by removing the need to solve very complicated differential equations, and instead solving a relatively simpler transcendental equation. Believe me, this a big deal.

And that's the basic physical background behind my code `p-winds`: I use this simplified formulation to model the upper atmosphere of planets (these atmospheric regions are also known as planetary coronae). Also, it wouldn't really be that useful if didn't put a star near the planet, so when you shine a bright star on this model, the hydrogen in the upper atmosphere can ionize due to the strong stellar irradiation (essentially stripping away electrons from the hydrogen atoms).

Alright, now let's get our hands a bit dirtier here. My biggest difficulty when writing this code is that I found it hard to wrap my head around the calculation of the ionization steady-state, which is, yup, you guessed it, a differential equation. The problem is that the inner parts of the atmosphere will depend on the ionization state of **all the layers** above it in the first place! So, to deal with that, my idea was to start integrating the differential equation from the outermost part of the atmosphere and inwards -- or at least that's what made sense to me. And it seems to have worked, because the end result is consistent with results from other models in the literature.

Alright, but what is the point of the model? Well, we can use physical models like this to help us interpret observations of atmospheric escape in exoplanets. Since the main gases that evaporate are hydrogen and helium (the lightest chemical elements), simplified models like the Parker wind are very effective at interpreting observations made with the *Hubble Space Telescope* and ground-based facilities too \[[^4]\].

Anyway, if you are also an astronomer and likes exoplanet atmospheres, feel free to take a look at the code. I made a self-imposed commitment to create a software that is fully open source and documented, so anyone can use it in their research! Also, anyone with a GitHub account can contribute to the project by submitting issues or pull requests. I have many plans for the future with `p-winds`, like implementing the helium steady-state to interpret He spectroscopy at 1.083 𝜇m, and hydrogen excitation to describe atmospheric signatures in H𝛼. Currently, `p-winds` is an alpha release, meaning that it is pre-release and not really ready for production yet (in this case, for scientific publications), but I plan on developing it steadily within the next months.

----------------

[^1]: test.

[^2]:

[^3]:

[^4]:
