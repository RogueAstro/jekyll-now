---
layout: post
comments: true
title: Ethics in machine learning 
author: Leo dos Santos
permalink: /blog/:year/:month/:day/:title:output_ext
tag: 2020
excerpt_separator: <!--more-->
---

Recently I have been delving into machine learning for a few reasons, mostly out of curiosity and because I think it is an important skill for a scientist like me. At the same time, we are aware of many issues on how artificial intelligence algorithms are deployed, such as consumer exploitation and social discrimination. How do we deal with this conundrum?

<!--more-->
{:refdef: style="text-align: center;"}
![Machines](/blog_assets/2020-12-19.JPG "Machines")
{: refdef}

In physical sciences, I have seen many people who write software to append a note saying that their software should not be used to develop military technology— the plotting software [`supermongo`](https://rhpcs.mcmaster.ca/~monger/sm.html)\[[^1]\] comes to mind. To cite an extreme example, in the past society saw many physical scientists contributing to the development of military technology \[e.g., [^2]\], and this left a sour taste in people’s mouths in hindsight. Now, I do not think this is a completely fair comparison, but what if we are also using machine learning (ML) and artificial intelligence (AI) technologies in a way that brings more harm than good for society in general?

In a nutshell, ML technology works more or less like this: you feed data to a computer, run it through specific algorithms, these algorithms optimize pre-determined functions that can describe the data input to the computer (i.e., they “learn” how the data behaves), and in the end the computer can make predictions based on the data fed to it. So, for example, if you have thousands of photos and you classify these photos and feed them to an ML algorithm, the computer can classify other photos that it has not previously “seen” based on what it learned from the data you fed to it. The same process can be done to learn the behavior of many things, including human beings, based on data collected from them.

Nowadays, ML tech is used in numerous applications in our lives, the most prominent being customer service, social media, autonomous driving, and predictive analytics. But other less known applications also exist, ranging from military training to agriculture. In an article recently published on *Nature* \[[^3]\], the chemist S. Lo Piano discusses several ethical implications from the use of ML tech in our daily lives. Some of the most upsetting traits of how these tools are deployed includes issues of social discrimination, threats to democracy \[[^4]\], and how they can be used to exploit vulnerabilities of consumers \[[^5]\].

Predicting the behavior of consumers is not something new. Society has been doing that since trade was invented a long time ago. What ML techniques can do is to make these predictions at an industrial scale, and with an accuracy that humans cannot always achieve. But that is just a means to an end. The problems arise on how these tools are deployed, and what they are used for. The interests of companies are not necessarily in line with the interests of the consumers, and companies are willing to do anything allowed by the law and regulations to increase their profit.

So, what sparked me to start researching the subject of ethics in ML tech is one particular tool — I’m not naming all the names — created by a Google employee. The example that the employee cites in their website is the following: this ML tool can be used to predict how someone playing a mobile game will either pay money to continue playing after a “game over” or will simply abandon the game, and developer can deploy incentives to retain this player and keep them hooked to the game. It goes without saying that similar perverse approaches are used to retain social media users as well. This is an example of how companies can use ML to maximize their profit at the expense of the consumer’s valuable time and attention.

But this example I described above is peanuts compared to the sort of insidious damage some AI algorithms can cause to individuals that happen to be part of a marginalized social group. In an article published on *Science* \[[^6]\], Z. Obermeyer and collaborators point out that an algorithm widely used in US-American hospitals to designate patients to health care providers is systematically racist. They found out that this algorithm is less likely to allocate Black patients than equally sick white people to extra care programs. According to the authors, this bias stems from the the fact that, statistically, Black patients spend less money for the same level of health care need, thus the algorithm falsely concludes that they are healthier than white folks.

The implications of ML tech in our lives has seen a staggering increase in scrutiny since 2016 \[[^7]\], so this discussion is anything but new. Fortunately, governments of developed nations are beginning to regulate ML and AI technologies \[[^5]\], but pressure from society is still necessary to make our concerns heard. A complete abdication of ML is obviously out of question seeing how many benefits it brings, but its use in our daily lives cannot be taken lightly. We must strive to respect the interests of stakeholders and communities in this context. 

--------------

[^1]: Do not use `supermongo`. I recommend an open-source alternative, such as [`matplotlib`](https://matplotlib.org).
[^2]: [Wikipedia article on the Manhattan Project](https://en.wikipedia.org/wiki/Manhattan_Project).
[^3]: Lo Piano, S. "Ethical principles in machine learning and artificial intelligence: cases from the field and possible ways forward," Nature Humanities and Social Sciences Communications 7, 9 (2020). [https://doi.org/10.1057/s41599-020-0501-9]()
[^4]: O’Neil, C. "Weapons of math destruction: how big data increases inequality and threatens democracy," 1st edn. (2016). Crown, New York. ISBN: 0553418815.
[^5]: De Sutter, P. "Automated decision-making processes: ensuring consumer protection, and free movement of goods and services." [https://www.europarl. europa.eu/meetdocs/2014_2019/plmrep/COMMITTEES/IMCO/DV/2020/ 01-22/Draft_OQ_Automated_decision-making_EN.pdf]()
[^6]: Obermeyer, Z., Powers, B., Vogeli, C. & Mullainathan, S. "Dissecting racial bias in an algorithm used to manage the health of populations," Science 336, 447–453 (2019). [https://doi.org/10.1126/science.aax2342]()
[^7]: Jobi, A., Ienca, M., Vayena, E. "Artificial intelligence: the global landscape of ethics guidelines," Nature Machine Intelligence 1:389–399 (2019). [https://doi.org/10.1038/s42256-019-0088-2]()
