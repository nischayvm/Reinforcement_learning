# 08. UCB 1 Theorem

- Playlist position: 8 of 60 (selected range: 1–34)
- Video: [UCB 1 Theorem](https://www.youtube.com/watch?v=7IA6Zb7KZM0)
- Caption source: English — NPTEL Verified
- Raw captions: [08_7IA6Zb7KZM0.en-6UJrWS5jR_I.vtt](raw/08_7IA6Zb7KZM0.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:24](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=24s)

Do you remember how many classes do we have for bandit algorithms, 4. you will try okay fine because the rate at which I am going I will probably need one more class just to finish the two proofs I wanted to do today so which should mean that I would need one more extra class for finishing all of bandits did we do 4 classes last year 6 yeah I think I we did we even had visiting faculty give a talk hmm...okay. We have 4 oh good fine

### [00:01:27](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=87s)

then I am not too bad okay. So instead of writing the cumbersome 2 ln n by s all over right so I am defining that as Cns okay then if I write Cn-1s it is ln of n-1 divided by s and then I can do C n, s + 1 so on so forth right I can just like a function just substitute that will make my life little easier right so the goal now as I mentioned earlier is to upper bound this expectation right so I will never play a suboptimal arm more than this many times okay that is essentially what we are trying to show okay

### [00:02:28](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=148s)

so one other notation I will just adopt the notation used in the proof here even though we introduced a different notation in the previous class for the same thing okay it makes it little easier for me. This notation indicates a I mean it denotes a random variable corresponding to that indicator right so this is a random variable whose value 1 if I t equal to i whose value is 0 if I t is not equal to i okay so whatever is this I will put in some kind of events here later right so if I t equal to i, then what does it mean it means that okay fine I apologize for the confusion this yeah so when I say I n equal to i, okay it means that at time

### [00:03:32](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=212s)

n I played arm i, right so if this the whole expression within curly braces will be one if at time at n I played arm i, it will be 0 if at time n I played some other arm not i okay so there are couple of things which we can observe about this so at any instant I n equal to i will be 1 for some i for everything else it will be 0. Right because at very time instant I can play only arm and at every time instance I will play at least 1 arm okay so it will be 1 for one of the arms for everything else it will be 0 okay this yeah the paper is not really the most accessible of papers out there right

### [00:04:49](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=289s)

so if you are going to read it on your own you will have to do some some work okay so things are not I mean they just assume that you are all really really smart people reading the paper so since some of the gaps you will have to fill in yourself right I am just doing one of the proofs in the papers so if you want to read the rest of the paper and understand all the theorems and all the algorithms that they describe in the paper. So you will need to do some additional work okay so L is some arbitrary positive integer so I start off by saying this.. okay so the number of times I have played arm i up til

### [00:06:07](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=367s)

the nth instant will be one which I get from the initialization plus k+1 because obviously I couldn't have played that arm again in the first K times right in the first K times I will play each arm only once right so arm i also I would have played once so in the first K trials the summation will be just 1 so I just have that 1 there and from the k + 1 th trial till the nth trial, I add the number of times this variable is 1 what does it mean number of times I have taken arm i right so I m will be, I m equal to i will be 1 whenever I take arm i so I just sum this up so that so that the number of times I played arm i is what I get right. Is that fine, this expression is fine okay this is the only directly intuitive part that we have here so after this no no after this whatever you do, these are all standard tricks

### [00:07:08](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=428s)

that people play to bound random variables okay so to actually tell you about the general techniques for all of this, I recommend you take the ATTOC course because about third of the course is all about how to do proofs like this right how many of you have done ATTOC already advanced techniques in theoretical computer science theory of computation. Okay that is a course that Jayalal Sarma teaches in the CS department so it is very relevant to lot of ML researches because more lot of machine learning has become like randomized algorithms right so if people teach you how to analyse randomized algorithms you can take the same ideas and use them in analyzing machine learning algorithms as well so lot of the tools that are developed there are useful here and many of the things that we do here right essentially have their roots in the kind of analysis that people do for randomized algorithms okay.

### [00:08:09](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=489s)

Any way we so we will start off by doing that so I have an arbitrary number l okay I say that okay fine let us assume that I have played the arm l times okay then let us start counting right so assuming that uptil the m-1 th step okay I have l or greater than l right only then I will count the arm pull so at some point I have discovered that I have pulled

### [00:09:11](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=551s)

arm i okay should I add it to my count or not what I do I will go head and look at the cumulative count so far if the cumulative count is l or higher I will add it to my count if it is below l I do not add it to my count because I am anyway starting my count from l okay. So this is slightly different way of doing that this is saying that I will start the count from some arbitrary number given that I have taken that arbitrary number already right so later on we will essentially now are going to bound this expression assuming that at least l times I have taken the arm right and then we will derive a bound for l so that we get whatever probability we want okay so that is the idea behind doing this so this I can now derive a bound for this assuming I have done at least l times right then I will go back and find what is that value of l so that I get whatever probabilities

### [00:10:12](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=612s)

I want right whatever guarantees I want I will go and find that l okay that's essentially what we are going to do here.

### [00:11:21](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=681s)

Okay I just need more notation here right this let me try this any way so when am I

### [00:12:39](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=759s)

going to take arm i right when will I take arm i when arm i has the highest where is this thing right when arm i has the highest value for this quantity right when will I take arm i when if that has the highest quantity among all the arms. Specifically I will take arm i only when Q plus C so that root term is now C right that root term there is what I have written as C so I will take arm i only when Q plus that C term is greater than Q of a star plus the C terms corresponding to a star. Yes that is why I have my lesser than or equal to here see at specifically this should be true right in fact it has to be larger than everything else right but at least it has

### [00:13:41](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=821s)

to be larger than a star correct so it has to be larger than every other action but like he rightly pointed out so this is a larger set than when I will actually be taking the action but that is okay because I am only trying to upper bound it right I am not trying to give an exact number because trying to give an exact number makes it too involved right I am just trying to give an upper bound so I'm saying very specifically I am looking at the best arm I am saying that this should be better than the best arm. At least right so anything else we need to have we will still need to have this right that condition is also there so I will put that condition back in right what does this curly bracket mean it is the curly bracket is a random variable that indicates it will have a value of 1 if the expression within the curly bracket is true it will have value

### [00:14:43](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=883s)

of 0 when the expression within the curly brackets is false so essentially this summation counts how may times this inequality becomes true after I has been taken l times right so that is what we did here right so this counting is whatever we are doing here is after l times i has been taken because l I have added here as a count so likewise I am counting the number of times this inequality becomes true after i has been taken l times. So this is essentially what I have so far right. Where? Here, this entire thing there is a seat vacant here and there is another seat vacant here if you want to move as well you can see everything you guys are all fine right you don't want to complain because I

### [00:15:56](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=956s)

will tell you there is a whole row vacant here no can't you see what I have written or don't you understand what I have written well subscripts become small right if you write them large then it becomes confusing so that is C m-1 for people who cannot read it I am reading it out that is C m -1 , T a star of m-1. That is basically the number of times I have played a star uptil the m-1 th point right note that I do not have to know this because I do not know what is a star right this is just the there but you know that there exists a a-star right and I know that my i has to have a better whatever that quantity than a-star right so its just that right I do not know I do not need to know which is a star okay just do not get confused by the fact

### [00:16:56](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1016s)

that I am using a star in the proof right did you get that C m-1 , T a-star m-1 and this is C m-1, T i of m-1. No a-star is the true true best action which you do not know anything about right because for regret we have to compare against the true best action right so we are comparing against the true best action right okay so far so good people can people who could not see heard me right and people understand what is going on right so now we will I'm shifting over here. My God for writing one line I am talking for 10 minutes man. I really need to have an additional

### [00:18:49](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1129s)

index for the Q-function for us to say these things, right. What I wrote there is m-1, so the Q-function at step m-1 okay, I really need that additional thing because Q keeps changing over time right so I need to know at what stage I am talking about the Q-function, so at that point I am talking about the Q-function at the m-1 th stage, right. Remember that the Q-function at the m-1 stage can be the same as the Q-function at the m th stage if I had not taken the action previously. At the m-1 th stage if I am not taking action a or action i, then at the mth stage also the Q-function of action i will be the same, it wouldn't have changed, right just you have to be careful about how you interpret the index and I hope I also do not mess it up

### [00:19:52](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1192s)

when I do these things here. No so we do read the different interpretation for and I do need an additional notation I apologize for that because we need to what we need to insert into this bound here. is the number of time I have taken a-star so far, right what I need to insert into this bound, is the number of times I have taken a-star so far which is T a-star m-1 right and so it become a little cumbersome now this can be is this will be T a-star of s okay

### [00:21:16](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1276s)

fine we can get away with that. This is a little weird expression so what I am saying here is okay take the minimum of this expression okay over all time instants 0 to m. Take the maximum of this expression right for all time instants l to m okay and look

### [00:22:17](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1337s)

at the number of times one will be higher than the other, right. This will be a over count of that event this is clear right but here I am talking about this quantity being higher than this quantity at that particular instant right I am talking about some time m-1 where the quantity for a-star was lesser than the quantity for i. I am talking about sometime instant m-1 at which this happened here what I am talking about, okay at a time m-1 right I look at all the a-star values I have had in the previous time steps okay, I will take the least of that, right and I will take all the i values Qi values I have had in the previous time steps I will take the max of that okay. If the max of this is greater than the min of that then I will count that as 1, right so can you convince yourself that, that event will certainly be counted right because at

### [00:23:22](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1402s)

that instant the value is already greater so obviously the max will be greater than the min right so if this is not the min, right the min should be lesser than this and if this is not the max, then the max should be greater than this. So if this value is greater than this value then the some quantity greater than this value will certainly be greater than some quantity lesser than this value right you can see that right, so this is just a over count of that event, right why am I writing this over count? Because it makes it easier for me to, sorry, now that is the event right the curly brackets makes it easier for me to write a expression. Yeah what is it, one second I will come let me finish. yeah 0 less than s less than m,

### [00:24:40](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1480s)

l less than or equal to Si less than or equal to m because l because I have that condition there right I have to have taken this at least l times, so the first l times what happens I do not worry so I will remove that right so only after that I am worried about, but this will be an over count okay this will be an over count of that. So little tricky

### [00:25:58](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1558s)

here so now the proof actually assumes that at this point, okay. I have taken this at least s times not T a-star s times okay, it is mainly because there is the notation translation problem but we will see we will work with this and then I will probably adjust the results later, right. But if you are reading the proof I am just telling you there is a mismatch in the notation that we have used so far, okay. But this is the neat trick that we have downed at, right. We have taken rid of all the Min Max and everything, right, So what are we doing here so assume that the Min occurs at some index right let us call that index, I do not know p, p1 let us assume that the Max occurs at some index say p2 right, so now what I am doing here is I am summing over all possible indices for a-star and I

### [00:27:01](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1621s)

am summing over all possible indices for i, correct. So the combination p1, p2 will occur somewhere because I am summing over all possible indices, right. At some point I would have used p1 for s, and p2 for Si, correct because I am summing over all possible indices right so what was p1, p1 was the one for which this minimum was achieved p2 was the one for which this maximum was achieved, so when I am summing over s at some point s will have p1 at some point Si will have p2 right, at that point this expression will surely be true because I know from the Min and Max argument that we had earlier that will be true. So I will certainly be counting this right I will be over counting I will be counting other things also but I will certainly be counting this, so essentially so far we have not lost anything we are essentially still maintaining at as Upper bound okay, so we started off with this event right now we have done a lot of simplifications and kept loosening

### [00:28:08](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1688s)

the bound, this was a strict equality and there was nothing here, right. This was strict equality no approximation here, so from there at every step I am essentially counting a larger and larger event, now the thing is I have come to a point where I have a simple enough expression right that I can try to bound directly now, okay. So you can start thinking you know this kind of should lead you to the Chernoff-Hoeffding bound I can use the bound, Chernoff Hoeffding bound to try and bound this expression. This is simple enough expression, okay. So if this is true, okay this is true when can this happen? So my claim is this can be true if one of several conditions hold right, so this can be true if, okay this can be true if I am either I am grossly under estimating

### [00:29:59](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1799s)

my optimal actions value, right. So this is my optimal actions estimate now this is the true value right so the true value minus the confidence bound. Or the other way around think about it, right. This Qs a-star plus the confidence bound is less than the true value that means I am grossly under estimating the true value that is one thing right. So that could be one condition under which this could be true what could be another condition you are grossly over estimating the ith value you are getting it, so either I have to make a big mistake for my Q star, a-star or I have to make a big mistake the other way for my i right you see that, right. So I have to either come very down from a true Q star value I mean a Q star, a-star or I have to be much above my normal value otherwise this is not going to happen, right.

### [00:31:00](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1860s)

So second condition is, okay. Or when can it happen without me grossly over estimating or under estimating it? When the true values are close right if the two values the a-star value and the i value are close to each other then I really do not have to grossly under estimate these things. So it is possible that I still could make errors, right. So essentially the other condition is right so I have my twice my I take the confidence interval right so I have a confidence

### [00:32:31](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=1951s)

interval add here I will have a confidence interval I will add from that side, right. So I will add a confidence interval right so I am taking twice the confidence interval from my lower value right, from the lower value I take twice the confidence interval. And if the upper value that is the optimal actions value lies within that right then I can make a mistake without making a gross error also, right essentially I am saying that these two are close together, right. And close is a relative term close is defined in terms of the current uncertainty I have, right. Because this is going to change every time I take an action this is going to become smaller and smaller, right. So at the beginning of the learning this can be fairly large so I can still make a mistake right even if the means are slightly far apart, right. So do you see the 3 conditions one of this at least will have to be satisfied for this event to become true, second one

### [00:33:36](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2016s)

says I mean second one is easy man, so the first one says okay I have my Q of a-star and I have my confidence bound this is the first one okay and the true Q star, a-star is there, okay. That means I have grossly under estimated my Q star a-star this is one condition, so the second condition says this is Q of i right and this is Q star of i, so grossly overestimated by Q star of i that is essentially what the second condition says so this is Qi is greater than Q star i plus the confidence bound so this is the confidence bound so Q star i plus this confidence bound will be only till here, right. But Q i is greater than that.

### [00:34:38](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2078s)

Whats that, No, no this is yet another condition that can hold right when both of these do not hold also I could still be making a mistake right I could still this could still be one if the true means or not far apart with respect to this error bar I have. See basically what I am saying is, a true Q star could be somewhere here right but I still can make a mistake because it is too close. So probably draw all this pictures and put it somewhere permanently. Because every time I seem to be re-creating these pictures, right. So I have the first thing I said okay the Q * is somewhere there right I make a mistake right so and then I

### [00:35:44](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2144s)

have this guy right so its possible for me to make an error, right and then the other case was okay this the true Q was somewhere here it is possible for me to make a mistake right this third case says no none of this really need to happen, right the true Q stars could be well within the bounds right, but given the current uncertainty I have in my Q of i right, so the true means are not so far apart right this this uncertainty cannot overwhelm it right the true means are actually within the uncertainty. Therefore, I could still make a mistake so the first condition is not true the second condition is not true but I still made the mistake, okay.

### [00:36:45](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2205s)

So people have all of this expression everyone has in their notebooks people who are writing notes, people who are not writing notes you have this in your memory, okay because I am going to erase it but I am going to need it again, okay so I want all of you to remember this. Okay, so let us look at 1, so I want to look at the probability that a-star so I want to

### [00:38:30](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2310s)

bound that probability, right so can I do that remember I told you Sn is capital Q, I told you mu is Q star right, so we have that already right, if you remember when I wrote down the Hoeffding Chernoff bounds, I told you the comparison right, I told you that Sn is capital Q, mu is Q star so you have those there, right. So essentially then your epsilon becomes C m right and my bound is e power minus 2 epsilon squared n right, and what is Cn so it is 2lnn by s squared. Plug it in, simplify it and tell me what is the answer? So what is your n there, now what

### [00:40:10](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2410s)

is the n that you have you to plug in to the expression, s this is where the thing became a little messy because the paper uses s as the, I mean they introduce an additional notation, right but I did not use that I try to use the T star, T a-star notation itself, so it becomes T a-star of s that is the thing that you have to plug in, okay so simplify it and tell me what is the answer. So I plug in T a-star of s here m here right, and then I have to square it basically that is my epsilon that will get squared, right so my T a-star of s and my T a-star of s get cancelled, right I will get ln m come on, after all that we have done so far you could

### [00:41:12](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2472s)

do this simplification easily enough just substitute this into that and then cancel things out and tell me what is happening. 1 by m power 4 right, so essentially this will be less than or equal to okay, so what about the second term okay hmm...phew, what about the third term okay, here is where we

### [00:42:38](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2558s)

are going to use our mysterious l right, what did l, what did I introduce l for I said that hey, I have done so many number of trials already, okay I am only looking at these events after that many number of times I have taken arm i, right. So I am going to make the following statement if I have taken sufficient number of trials initially okay, if I have taken sufficient

### [00:43:43](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2623s)

number of pulls of arm i initially this event will never happen that is what I am claiming, right this is rather easy to see right, so what do we have, we have q star a-star minus Q star i minus 2 Cm.. okay right. So essentially I am saying that my Ti Si is at least this

### [00:44:50](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2690s)

much, right so that is what this means right okay, when I say l is equal to this much that means the number of times I have taken arm i is at least this much. If you remember my Si summation starts from l right, I consider Si only from l so if say l is this so that means my Ti Si is at least this much, correct go and plug this into my C ns expression. So if my s is this much, at least this much, so what do I get, I get 2 by 8 ln m and my delta i squared will go up so ln m, ln m will get cancelled, right so 2 by 8 will become 1 by 4 that is half, half into delta i right, so half and 2 will get cancelled I will essentially

### [00:45:52](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2752s)

get delta i, right so this expression will become. Right and what is this equal to, so for any value of l greater than this, this quantity will be greater than 0 that means this inequality will never hold, correct do people see that, you want me to do that again, yes okay, so I am saying l is going to be at least this

### [00:46:53](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2813s)

much so then if you remember my Ti Si that the Si summation is starting from l, I am assuming that at least l times I have taken this already, right. So I am assuming you have taken this l times already so what I will do is I will plug the, this value for the number of times I have taken this already right this value, so I will plug in 8 ln m right this is C m,s right so in this case look at the expression m, this so this will be ln m right I am plugging in here instead of s, I will plug in 8 times ln m divided by delta i squared right, ln m, ln m will get cancelled so 2 by 8 will become 1 by 4 and divide by delta i squared will go up right, so I will basically get root of delta i squared by 4 which is delta i by 2, right. So I will come and plug in delta i by 2 here, 2 and 2 will get cancelled I will essentially

### [00:47:55](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2875s)

end up getting delta i here, so that is what I have written here. So and by definition of delta i this expression is 0, right and for values larger I mean if I take the action i more times then this will essentially become greater than 0 and therefore that inequality that I wanted will never hold, if I have taken l at least, if I have taken action i at least l number of times where l is given by that expression. The third condition will never hold, okay so the probability of the third condition holding is 0 if l is greater than this, right. So now what happens so the probability of this whole thing happening is upper bounded by just two times this probability right, just add these events up so we are still not done. Where are we, so we are bounding the

### [00:48:59](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=2939s)

expected value of that thing right, so we have expected value of, so and I am going

### [00:50:11](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=3011s)

to ask you to write this out here okay. So this is lesser than or equal to 8ln m by delta i squared because that is l plus these summation terms that we had earlier right, and I am substituting a specific value for l here okay, then what will be the internal term here. Remember, we had this random variable which could take values of 1 or 0 so what is the expected value of the random variable is just a probability of it being 1, right so there are only two of those things right. So the probability of this event plus the probability of this event, right that is basically it so I am not writing down this because these expressions are going to take a long right so the probability of this event plus the probability of that event so in which our case is just m-4, m power -4 that is essentially, right so it is clear. So you see how that came about, right so here this was the random variable right. Now once I took the expectation

### [00:51:19](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=3079s)

so I can replace that random variable with the probability of it being 1 that will be the expectation of that random variable, okay is it fine so replace that with the probability of it being 1 is upper bounded by m -4, m -4 and that is basically here, okay great. So this summation okay, I am going to declare it to converge to 1 plus pi squared by 3 okay, you can its little involved thing but it is pure algebra again I mean you can work it out, okay or I mean this is a standard relation you can look it up also, right so that is

### [00:52:20](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=3140s)

basically what we have. So this is kind of see that this is going to because this is going to be a diminishing sum so it is going to converge to a limit, right and so what is really interesting is this part, right it is some constant whatever it is that it converges to it is not really of interest you know not really of great interest what is really of interest is this 8 ln n by delta i, right. Because this is the one where you are going to get messed up a lot because it has the ln n term right, and it also has your delta i squared, right but this is the only expected value of T i n, right you have to multiply it by delta i to get the total regret and you have to sum over all i, right so that is essentially the thing that we have finally that expression that I erased here that is what you will end up with that is why I said keep that in your mind because that is the final expression you are going to end up with, right. This is for each arm this is for one suboptimal arm, right this is the total number of times

### [00:53:25](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=3205s)

you have played it right that is all we have derived now, so the regret due to that suboptimal arm will be delta i times this number so that is why the delta i squared goes to delta i in the denominator in the original expression if you flip back and you look at the original expression we had a delta i here and we also had a 1 plus pi squared by 3 into delta i. but this is for one arm, so you have to do this for all the suboptimal arms basically that is why your summation is over all i which is not optimal, okay great. So this is you have done with UCB and you have shown that UCB's regret is bounded and what is the nice thing we have shown here is that the regret grows as ln n right, and there is a result from the 80s which tells us that you cannot have a regret optimizing algorithm that does better than ln n, right what you can try to improve on is the 8, right this is also impossible to get rid of, the delta

### [00:54:31](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=3271s)

i is also impossible to get rid of you cannot say that I will, I mean if the arms are close in reward right, it becomes hard to eliminate the bad arms, right. If they are far away in reward then you can quickly figure out which are the bad arms but if the arms are close in reward and it becomes harder to figure out so those things are always there. So those are essential components to it so basically people fiddle around with that 8, okay and yeah so that is essentially the lot of work that happens in regret optimality so I will have to stop here because we have reached 5 o clock I do not know if how many of you noticed it so if you have not I will take that as I kept you successfully engrossed, but if people were just biding their time to leave well I apologize for keeping here for so long, but I needed to finish this right, I could not have stopped half way through and then start in the next class with 3 summations or something, right. So in the next class right, so we will look at the last optimality criterion I was talking

### [00:55:31](https://www.youtube.com/watch?v=7IA6Zb7KZM0&t=3331s)

about which was PAC optimality, okay. IIT Madras Production Funded by Department of Higher Education Ministry of Human Resource Development Government of India www.nptel.ac.in Copyrights Reserved
