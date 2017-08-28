# Projects-with-Ning
random stats and machine learning stuff
**Ning's code but inspired by Ian's dataset and written by Ian so there's a lot of profanity. Ning does not claim any responsibility for all the cursing. I don't either but whatever.**

# Today's topic: T-tests vs. Permutation Tests

<br />So. Which one is better?
<br />Who knows, so let the BATTLE FUCKING ROYALE begin.
<br />Or more correctly put - which test provides a better characterization of the data? How do we show what these datasets represent better?

What we did here:
<br />Say we have two datasets that are borderline significant at p = 0.05.
<br />Our question is - are these datasets significantly different IRL?
<br />So we're going to simulate an extreme case with small sample sizes. 

**First**, we do a t-test. Well, we simulate a t-test:
<br />We have a dataset A that has a mean of 1.24 and a standard deviation of 1.75, with a N = 10.
<br />Then we have another dataset B that has a mean of 1.78 and a standard deviation of 1.1, with a N = 15.

p.s. SPSS sucks. Obv. SPSS can't do this shit, because it don't do different Ns. Filthy casuals. #python-FTW

When doing t-tests, we have to assume:

1. independent sampling (every single subject is randomly sampled, aka, subject 1 and subject 2 and subject 3 are independently sampled. but they're not. but we can't do anything about dis. wtf, aka in psychology terms, wutever.)

2. normalization, aka normal distribution (personal note: I don't think any of the shit we test is normal a lot of the times, but let's thank Fisher's gargantuan legacy and the lazy-as-fuck posterity children that we are for just going with the flow)

3. equal variance (we can assume both cases: equal and non-equal variance, so we will below (because we be thorough))

<br />/begin rant
<br />So what this means is that, in using t-tests, we generally and literally violate every single assumption in any fucking psych/neuro/#FAKE-scientific study we do. 
<br />So why do we use t-tests?
<br />Because there are no better alternatives. p.s. but it don't have to be. We are the purveyors of dis light, the deus ex machina of your statistical nonchalance.
<br />/end rant

ANYWAY, **results, results, results**. 
<br />You can see on the Results + Blue-And-Yellow figure that we have generated two sets of data (datasets A and B) and t-tested them.
<br />You can also see that assuming equal variance and non-equal variance changes the statistical significance of the difference between the datasets A and B. #told-you-so #assumptions-matter
