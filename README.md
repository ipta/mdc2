# International Pulsar Timing Array Mock Data Challenge \#2

![IPTA Logo](/images/ipta_logo.jpg)   

Announcements
-------------

  * MDC2 is open and accepting submissions.
  * The deadline for submitting analyses for MDC2 is, <b>March, 15 2019</b>.          

The International Pulsar Timing Array (IPTA) is a galactic-scale gravitational-wave observatory that monitors an array of millisecond pulsars. The timing precision of these pulsars is such that one can measure the correlated changes in pulse arrival times accurately enough to search for the signature of a stochastic gravitational-wave background. As we add more pulsars to the array, and extend the length of our dataset, we are able to observe at ever lower gravitational-wave frequencies. As our dataset matures we are approaching a regime where a detection is expected, and therefore testing current data analysis tools is crucial, as is the development of new tools and techniques.

![IPTA Logo](/images/PTA_on_galaxy2a.jpg)

Here we provide the second IPTA Mock Data Challenge. The purpose of this challenge is to foster the development of detection tools for pulsar timing arrays and to cultivate interaction with the international gravitational-wave community. For more information about the IPTA mock datasets see the
<a href="https://ipta.github.io/mock_data_challenge/">MDC2 website</a> or the announcement on the <a href="https://ipta.github.io/mock_data_challenge/">ArXiv</a>.

In order to participate in an MDC just go to the IPTA <a href="https://github.com/ipta/">GitHub page</a> and fork the repository with the MDC you would like to participate in. Also, send an email to the Data Challenge Working Group Co-Chair,<a href="mailto:hazboun@uw.edu"> Jeffrey S. Hazboun</a>. This will allow us to update participants about new MDC releases and the currently open datasets. This README will record any announcements made about ongoing MDCs.

Summary of MDC2 Datasets
------------------------

In the following table we summarize the contents of the 6 different datasets included in MDC2. Details about the noise parameters injected into Group 1 can be found along with the datasets on the IPTA GitHub page in the form of a `json` file.

|Group.Dataset   | Time Span | Freq (MHz)  | Observing Cadence |  Noise | Signals  |
|---|---|---|---|---|---|
|g1.d1a(b) | 15 yrs | 1440  | 30 days | WN | SB|
|g1.d2a(b) | 15 yrs | 1440  | 30 days | WN,RN | SS |
|g1.d3a(b) | 15 yrs | 1440  | 30 days | WN | SB+SS|
|g2.d1 | 15 yrs | 800, 1440  | 30 days | - | - |
|g2.d2 | 15 yrs | 800, 1440  | 30 days | - | - |
|g2.d3 | 15 yrs | 800, 1440  | 30 days | - | - |

WN=white noise, RN=red noise, SB=stochastic background, SS=single source

The datasets included in MDC2 include parameter files containing the timing model parameters for a pulsar, and timing files containing the integrated times-of-arrival or TOAs of pulsar pulses.
These files are referred to as `par` and `tim` files, respectively.

The TOAs in the `tim` file contain Doppler shifts from the motion of the Earth in its orbit, relative proper motion between the solar system and the pulsar system and any orbital motion of the pulsar, if in a binary system. The `par` files contain the relevant parameters needed to construct such a model to remove these effects, but its construction is left to the participant.
In addition, various clock corrections, observatory location coordinates and other observation dependent effects must be taken into account to build an adequate timing model for a given pulsar.
There is a rich history in the pulsar timing community of scientist-written and maintained code bases useful for timing pulsars and, more recently, for doing gravitational wave analyses.
While the participant is free to write their own code, there are three publicly available sets of software for modeling pulsar TOAs,
<a href="http://tempo.sourceforge.net/">`TEMPO`</a>, <a href="https://bitbucket.org/psrsoft/tempo2">`TEMPO2`</a> and <a href="https://github.com/nanograv/pint">`PINT`</a>.
While new software development is welcome, the participant is encouraged to use one of these existing packages for building a pulsar timing model, and to focus their time on the data analysis algorithm development.

Use of Existing Gravitational Wave Analysis packages
----------------------------------------------------

The existence of a number of well developed PTA <b>gravitational wave data analysis</b> packages needs to be recognized and commented on here.
Among the many reasons for holding a MDC, two are relevant when discussing these previous code bases; to encourage new researchers to become involved with PTA data analysis and to foster the cross pollination of analysis techniques.
In order to facilitate the first of these, the development of an entirely independent code for PTA analysis is not required for participation in the MDC, though obviously welcome and encouraged.

Besides the existing analysis codes (<a href="http://tempo.sourceforge.net/">`TempoNest`</a>, `42`,
<a href="https://github.com/jellis18/PAL2">`PAL2`</a>, <a href="https://github.com/vhaasteren/piccard">`piccard`</a> and <a href="https://github.com/stevertaylor/NX01">`NX01`</a>...) there also exists a code built as a framework for constructing a PTA analysis developed by the NANOGrav collaboration, called <a href="https://github.com/nanograv/enterprise">`enterprise`</a>.

Since these tools are accessible widely, we do not prohibit their use in the MDC, but will categorize them differently when discussing them in any manuscript that summarizes the MDC.
Entries based on an existing code base (unless submitted by the developer of that code) must add some significant new ability to the base code in order to warrant their submission, and, of course, cite the original developer. An example of such an addition could be a new way of modeling noise in a pulsar, or using the output from the original code to calculate a different statistic.

If you have any questions please contact <a href="mailto:hazboun@uw.edu"> Jeffrey S. Hazboun</a>.
