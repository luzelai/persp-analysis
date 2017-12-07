Final Exam
================
Gabriel Velez
12/6/2017

Summarize Research Designs
--------------------------

Edelman and Luca (2014) take an observational approach to exploring discrimination on Airbnb.com. Specifically, they use observations of listings on Airbnb to ask if asking price of a host is related to his/her/their race, while holding constant other factors related to the price of a rental (e.g. number of people accommodated, location, social network presence, photos). The authors thus focus on the supply side and on the question of online marketplace discrimination dynamics (i.e., if there is a difference between the prices asked by Black and non-Black hosts). To do this, they collected “a snapshot” of listings from July 17, 2012 (specifically the price asked, the characteristics of the host, and the characteristics of the apartment) and then analyzed them for differences by race. The authors used workers on Amazon’s Mechanical Turk (MTurk) to rate the quality of each listing on a scale from 1 to 7 (which was used to control for quality of apartment), and then also to identify the race of the hosts. They first looked at the raw differences between Black and non-Black hosts in asking prices (and found a significant result). They also found a statistically significant difference when running a regression of price on race of host (Black or non-Black), controlling for other information a guest would see when looking at the listing. Controlling for these factors removed the effects of guest perceptions of location, quality, size, etc.

The research design of this first paper leverages computational methods by using mass collaboration with human computation through MTurk. Specifically, the authors employ a split-apply-combine method. They ask MTurk workers to look at a single listing and rate it, and then separately to look at a single host and identify their race. The authors then bring this data back together, with the first part helping control for the quality of the listing and then second part serving as the critical independent variable (Black or non-Black host). This approach takes advantage of the benefits of human computation because the task of assigning these ratings or race are independent, easily split, and have a clearly measurable outcome.

Edelman, Luca, and Svirsky (2017) use an experimental approach to explore how the race (specifically Black or non-Black) of a potential guest affects the rate of acceptance by the host. They also use observational data to explore the heterogeneity of treatment effect, such as how the discrimination against African American guest requests may vary by type of host. To do this, they generated requests from 10 “distinctively white” and 10 “distinctively African American” names for 6,400 Airbnb listings across five cities. Each host was contacted no more than once (and if they had multiple listings, then one was randomly chosen), and was randomly assigned to receive a request from a “white” named profile or a “African American” named profile. This use of randomization means that one could say that treatment assignment (i.e., being sent a “white” guest request or a “black” one) was independent of the characteristics of the host. The authors then analyzed the positive responses rate difference to these two groups of requests. Additionally, the host’s profile image was assessed for race, gender, and age using MTurk. This data was used to explore whether different types of hosts or different types of properties tended to show greater discrimination. They then validated this experiment with observational data by exploring whether or not a given host had an African American guest in their most recent guests. They used regression analyzes to see if there were differences by whether the host had a review from an African American guest and found a statistically significant result (i.e., that those without responded less frequently to their requests from African American guest names).

The computational methods that were used for this research were MTurk, similar to the other paper, as well as a face-detection API (Face ++) and digital scraping. Both MTurk and Face++ were used to categorize people based on race, gender, and age. First, hosts’ profile images were analyzed using a human computation split-apply-combine approach in which MTurk workers were asked to assess race, gender, and age. To address questions of validity, two workers assessed each image, and if they disagreed, a third was hired. If the third disagreed with the other two, then the authors manually coded the image. This data was then used to explore differences in discrimination by group. That is, once it was found that African American potential guests received fewer positive responses, this data on the host was used to examine if discrimination was more or less depending on the characteristics of the host. Face ++ was used to categorize the past guests of a host by race, gender, and age, which was then used to explore if there was a relationship between hosts’ prior guests and discrimination. Finally, the authors note that they collected all data using digital scrapers (to get profile photos, etc.), and the inquiries were obtained using web browser automation tools. These methods allowed for more efficient and cheaper data collection, as well as the ability to send out many more requests (and thus have a larger N and greater statistical power).

Effectiveness of Research Design
--------------------------------

The Edelman and Luca paper (2014) offers an interesting finding, but the underlying interpretation may be challenged without further studies to add greater validity and explanation. Through this observational research project, the authors find that comparable offerings from Black hosts are offered for less than from non-Black hosts. They note that their analysis only focuses on price effects because of the unavailability of data about demand. They then connect the finding to discrimination that is occuring based on race. Nevertheless, since they only focus on the host and the price effects, there are significant questions that one could have about this link. For example, do Black and non-Black hosts start by asking similar prices (and then does a lack of demand cause these to go down for the former)? The study is also observational, so we are still left wondering why (i.e., why do Black hosts ask for less? Is it because they are offered less, because they don’t believe they can make as much, because they are less experienced in doing this, etc.). The observational research design does not allow for causal explanations. Additionally, I would challenge the construct validity because it seems to me that what they are finding may not be related to the construct they want to study (i.e., discrimination) since there are these questions left unanswered and unclear.

A second issue with this project is that it only samples from one city (New York) and on one day. While one may find fault simply with the fact that it is cross-sectional in this sense, there are also serious considerations based on these specific choices. First, New York has a notoriously expensive and challenging rental market and high cost of living. It is also a setting of high desirability for tourists. Finally, it is a quite segregated city in terms of housing (see [this](https://www.nytimes.com/2016/04/15/nyregion/segregation-new-york-city-and-de-blasio-affordable-housing.html?_r=0) article and the report cited [here](https://danielkayhertz.com/2014/04/14/how-segregated-is-new-york-city/)). Second, data was only collected on July 17th. This date comes right in the middle of summer tourism, and there may be connected issues to this fact (e.g., it is possible, though I could not find statistics, that non-Black people may be more likely to be tourists and so a reason behind the difference may be in the consumer population specific to this date). Though each one of these possibilities might be small, there are clearly some issues with the external validity (the generalizability) of these findings to other populations and other times.

In terms of the use of Big Data, this study employs computational methods to explore differences in offered rental prices by race, but misses out on some of the key benefits. It takes advantage of non-reactivity (that these prices can be observed without changing them), while avoiding issues of dirtiness (since it is simply looking at offered prices) and sensitivity (since it is publicly presented information). At the same time, this research does not take advantage of the longitudinal possibilities of tracking prices over time (see the questions about “why” above), and faces real challenges because of the inaccessibility of the demand side of this platform. All in all, from this paper we can learn that there is a difference in the prices offered by Black and non-Black hosts for Airbnb rentals on a specific day in New York, but I would challenge a broader application until more research is done.

The Edelman, Luca, and Svirsky (2017) paper, in contrast, is able to address causal questions by running an experiment, but also raises other issues, including in relation to ethical questions. On the positive side, this paper uses an experimental design and random assignment well, providing strong internal validity and allowing a causal claim to be made. It also takes a dual approach to make sure the names are associated with the desired races by drawing from a list of most popular names by list and then validating that with a survey. In terms of external validity, it also covers five cities and 6,400 hosts (a high number that takes advantage of the possibility of Big Data collection to cover many observations). It is important to note that the initial goal was 10,000 hosts because of questions of sufficient statistical power (and that was not reached because of the site shutting down the experimental accounts), which may mean that 6,400 may not have been enough for strong external validity. At the same time, an external validity issue with much research on social media or internet platforms is often that they only focus on a specific part of the general population (those who use such services). In this case, the research question is specifically about discrimination and such online marketplaces as Airbnb, so this is not as much of a concern. Lastly, one could argue that extrapolating these findings about Airbnb to other online selling platforms (like EBay) may be beyond this research design, but the authors do a good job linking this to other research about other online marketplaces.

In terms of heterogeneity of treatment effect, the authors do a good job of exploring this question by looking at the different subgroups of hosts. In fact, part of the research goal was to explore if there were differences in discrimination by characteristics of the host (e.g., race, whether they had previously rented to African Americans) and the rental offering, so there was a specific goal of looking at the different ways that subgroups might respond to a potential Black guest. Another possible issue that the researchers address is the dirtiness of the data. They note that the majority of responses they received from hosts fit into 6 categories, but that for their analyses they restrict it to the simplest (“yes”). Nevertheless, they offer a reasonable argument for ignoring the categories other than unequivocal “yes” or “no” through demonstrating that the rates of the other responses are about equal by race.

Outside of the question about having a big enough sample size, two key critiques can be levied at this research project for system drift and for the lack of consent. First, as noted previously, the researchers were not able to collect as large an N as was their goal because of Airbnb shut down their experimental accounts. This could be thought of as a system drift in which the entire system is changing to avoid the possibility of being able to conduct this experiment. In addition, though this would not affect the experiment in and of itself, the authors do note that Airbnb has become increasingly aware of these issues around discrimination, and as the paper was in development, made some changes that may (or may not) help address discrimination on its platform. Issues of drift thus must be addressed in thinking through the lessons one can learn and what one can takeaway. Second, I would argue that there are ethical concerns with this study in terms of the lack of informed consent. While the research is certainly pertinent and serves a greater societal good, one could challenge that the researchers showed respect for persons. Hosts did not know that they were being included in a research project (which may have made their responses more “real” and avoided reactivity), and they certainly gave no consent to have their responses to inquiries to be included in research. Unlike the first study (where only publicly posted information was used), this research project actually interacted with the hosts, deceived them, and then used their private responses as data. While as far as I know it does not break any law (and thus upholds respect for law and public good), there is a pertinent question of if it took an ethical approach to conducting this research. All in all, this study shows us that there is very likely a causal connection that if a guest is Black (or, specifically, has a often-identified-as-Black name), there is a lower likelihood that they will be accepted by an Airbnb host, which is particularly the case if the host does not have a recent review from an African American. Even as we can say that we learn this from the paper and that it manages questions of validity, heterogeneity of treatment, and big data well for the most part, there are also ethical concerns about its design and how it was conducted.

Value-Added of Both Research Projects
-------------------------------------

In thinking about these two studies working together, it is important to first consider what methodological strengths and weaknesses they might bring in unison, and then also how their actual findings would provide more insight in conjunction.

In many cases, combining observational studies and experimental ones may be good for strengthening overall the validity of a research project. On the one hand, observational research designs often have strong external validity (because, for example they access a large number of data points and are based in “real-world” choices and action). They may have issues with internal validity since there is no control for who chose what (i.e., no randomization), and so their may be confounding variables. Experimental designs, on the other hand, may be good for internal validity (because of random assignment), but there can be issues of generalizability to other settings.

Thinking specifically about these two research projects, the first has some obvious issues in relation to validity (including construct validity), as mentioned above. By itself, it offers evidence that there are differences in the prices of comparable listings by Black and non-Black hosts, but it is difficult to assess from the data what the reason for this is. Also, the limited choice of focus for the data collected means that (in contrast to the case with many observational studies) it may be hard to generalize these findings as well. The second paper actually has relatively strong internal validity (due to randomization, uniformity in the treatment/control contact emails, and the process of picking the profile names) and external validity (for an experiment since the authors used five cities and a large number of hosts, even though they did not reach the number that was their goal). The second paper also incorporates observational data from Airbnb’s site to be able as well to get at heterogeneity of treatment effects. The second research project is a much stronger research design and would bring a lot more insight to the first, though the first may not help bolster or assuage the concerns with the second (which are more about ethics and drift).

Thinking about the actual findings, the two research studies target different aspects of the platform Airbnb. To this end, they each add a piece of evidence that such an online platform does allow for discrimination (or at least unequal practices related to race), which may be evident in both the ways that the sellers present their products, as well as the choices they make in selling the product (i.e., to whom they sell). In other words, adding together the two research projects that we read for this assignment does provide deeper evidence that there are issues around racial differences in user behavior on Airbnb (and in this way contributes to a larger literature on discrimination in online marketplaces). Nevertheless, since one focuses on prices offered and the other on response to guest requests, it is hard to say that they are exactly complementary or that the causal findings from the second can help explain the first. As a whole, they offer compelling evidence for issues of discrimination, and bring thus bring up important ethical questions about Airbnb’s structure and policies (and together, along with other research, may have helped create enough pressure to force Airbnb to make some beginning changes).

As one final point on this question of value added, I would say in general that it would be ideal to do an observational and experimental study both on differences in prices by race. In this sense, one could mix observations of both hosts and guests with experimental methods, which could be either similar to how it was done in the second paper or in a “lab” setting through a digital survey or experiment method with consent (such as through MTurk) in order to address ethical concerns. Using both approaches (that is, observational and experimental) would boost the validity, while also helping identify what differences by race exist in behaviors on the platform (which observational would be good for) and possible causal mechanisms (which the experimental part would illuminate).

Applying a Digital Survey-Based Research Design
-----------------------------------------------

The primary question of interest for these two papers focuses on whether or not Airbnb as an online marketplace enables discrimination (specifically between Black and non-Black/White hosts and guests). The first tries to do this by using observational data on differences between prices for listings of Black and non-Black hosts, while the second runs an experiment to see if there is a difference in responses to guest inquiries from “distinctively” white or African American names (and then uses observational data about the hosts to explore differences in this discrimination by type of host and property).

If one wanted to explore the same questions through a survey, there are obviously a number of different approaches, but one would be to ask questions about different potential guests and hosts. In other words, fake Airbnb profiles could be created (both of hosts and of guests) with the exact same criteria that are associated with price of listing (as the first paper notes, things like size, location, etc.) and hosts’ positive response (as the second paper notes, previous reviews, etc.). First, on the demand side, a group of people who use Airbnb as guests could be asked to rate the quality of a given listing and what price they would pay for it. On the supply side, a group of Airbnb hosts could similarly be given the profiles of guests and asked to rate how much trust they would have in this person as a guest and if they would respond positively to a request from a guest with this profile. A basic issue with this approach would be how to make sure that the different profiles/listings that participants were asked to rate were similar enough to each other to be able to say that the difference may be related to race, but not similar enough that the participant understands that racial differences are being explored (since they may then offer similar ratings simply to not look racist). This same issue is why it would not be a strong approach to survey guests and hosts and simply ask them straightforwardly would they rate listings from Black hosts or request from Black guests lower; social desirability bias - not wanting to seem racist - may skew their answers. Lastly, in order to get a large sample size, this survey could be run over MTurk and could even be randomized so that participants only get one type of profile (Black or non-Black). Their responses could be matched with other similar participants to analyze differences. In such a design, each worker would only get one type of scenario (and such randomization could help with internal validity and exploring causal mechanisms), but their responses would be matched with those of a similar group. This grouping would be decided based on the characteristics that have been shown to be important by previous studies, like the two for this assignment.

Another concern would be that people simply would respond in ways that are not consistent with how they actually act. In other words, they may rate Black and non-Black profiles similarly, but in a real-life situation as a host or guest, they would treat these differently. One possible way to address this would be similar to the second paper by linking survey data with observational data available on Airbnb. Two approaches could be taken: either the researchers could ask participants to give access to their Airbnb accounts or data (in the sense of what listings they have viewed, what messages they have received, etc.), or the researchers could use the publicly available data (i.e., for hosts who they actually rented to, and for guests where they actually stayed and their reviews). By using this enriched asking approach and linking the surveys with actual behaviors on Airbnb, it might be possible to corroborate or challenge certain of the survey findings. For example, there might be consistently equal rankings of Black and non-Black listings, but the same participants almost never rent from Black listings. A researcher would then have to explore why this might be.

Surveys also often face issues of motivation; survey respondents may experience fatigue, lack of engagement, and may simply be hard to recruit. In this case, since we would specifically want Airbnb users, we then limit our sample and it may be difficult to convince users to participate. Using Amazon MTurk and paying participants is one way to try to motivate participants. Another, though it would require the participation of Airbnb, would be to offer incentives linked to Airbnb. For example, if a host participates in this study, then they received a special boost from the site or are awarded the Airbnb fee of their next listing. This would help motivate the specific population of interest, but may be difficult because these two papers seem to indicate that Airbnb is not interested in supporting or addressing the findings of this line of inquiry about its online marketplace.