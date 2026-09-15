# 10. Median Elimination

- Playlist position: 10 of 60 (selected range: 1–34)
- Video: [Median Elimination](https://www.youtube.com/watch?v=3iNaR0Mq1ug)
- Caption source: English — NPTEL Verified
- Raw captions: [10_3iNaR0Mq1ug.en-6UJrWS5jR_I.vtt](raw/10_3iNaR0Mq1ug.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:08](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=8s)

Okay, good took a while to write so essentially what we do is we start off with K arms right

### [00:04:39](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=279s)

and then in the first round okay so median elimination is going to proceed in rounds okay. In the first round we pull each arm some number of times right determined by this magic quantity. So can people read this magic quantity it is 1 by epsilon l by two the whole squared, better? log 3 by delta l okay. So I pull each arm that many number of times okay and then I estimate their empirical value right Q l a I will estimate it where l indicates that this is the Q function I am forming at the lth stage okay. Then what I do is I take these Q l a, arrange them in ascending, descending

### [00:05:44](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=344s)

whatever order I find the median of all these arms. And then eliminate all those arms whose values is below the median right I am eliminating. So this is the set difference so I take my current set S l, right these are all the arms that are under consideration. So S1 will be all the arms and then I am eliminating all those arms such that so my Q l a is less than ml where ml is the median at the lth level right. And then I change my constants by magic amounts again. So my epsilon l plus 1 becomes three-fourths of epsilon l, epsilon l itself started as epsilon by four okay. Now it becomes 3/4 of epsilon by four and my delta l plus 1 becomes delta l by 2 which already started as delta by 2 so it becomes delta by 4, and l equals l plus 1 and I keep

### [00:06:47](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=407s)

going until my S l becomes 1, the number of arms left becomes one right. So how many rounds will I go log K rounds because every time I am eliminating half the arms right, because I am looking at the median and I am eliminating everything below the median. So I am guaranteed to eliminate half the arms in every round, so I will end in log K rounds okay. But the trick to provide proving any kind of sample complexity here is to show that okay, this quantity right when I sum it over this log K rounds is some bounded quantity right and that gives me the sample complexity I want. I have already told you what the sample complexity is going to be, what was it K by epsilon square log 1 by delta, some constant by delta, so as far as order notations we can ignore the constant so log 1 by delta. So that is what this is going to be the sample complexity,

### [00:07:51](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=471s)

so I will have to show you that first. Second in fact first I will have to show you that this is actually a pac algorithm right, that it actually gives you a epsilon optimal arm with a high probability right. It becomes a little tricky here, because I am eliminating half the arms every times. So now I will have to think about what is the probability that I have eliminated all the epsilon optimal arms right. So I have to, in some round along the way before I reach the final round okay I should not eliminate all the epsilon optimal arms right. So what we will do is you see that right, because at the end of the thing if that one arm left is some epsilon optimal arm, I am safe right if along the way if I eliminate all the epsilon optimal arms then I am in trouble. Right so what I will do now is to show that at every round the probability of me doing that is very small. So small that when I add up the probability of me eliminating across all the rounds it

### [00:08:52](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=532s)

is still below delta right it is still below delta so that is essentially what I am going to try and show did that make sense. So at every round the probability of me eliminating all the epsilon optimal arms is small, so small that when I add it up across all the rounds it is still less than delta okay. So that is essentially what I am going to what I am going to show. Okay so first theorem that I will state it, but I will come back and prove this later is the median elimination algorithm with takes epsilon, delta this is epsilon delta pac okay. So we will prove this in two parts the first lemma

### [00:10:46](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=646s)

will help us establish that okay, and then we will have another result later that will help us establish the sample complexity. Sample complexity is actually trivial right if you think about it, it is essentially summing this quantity up right starting from epsilon by four and delta by two and successively changing the value of epsilon and delta okay. It is just a bunch of algebra right you just move numbers around and simplify things you will get it conceptually there is nothing deep about looking at the sample complexity. So is that clear, so I essentially have to sum up this quantity right for every arm. So this will be multiplied by the size of the arms which will be, which will start with K and then it will become K by two, K by four successively becomes smaller and smaller and likewise the epsilon and my delta also becomes smaller and smaller. So the idea is to just to sum it over l this quantity and then replace this by a function of epsilon and l. You can

### [00:11:51](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=711s)

replace epsilon l right by a function of epsilon. So what is epsilon 1, it is epsilon by four, what is epsilon 2, three by four into epsilon by two, epsilon by four, epsilon 3 is three by four the whole square so epsilon l is essentially three by four whole power l minus one into epsilon by four right. So like that so you can write this a similar expression for delta and we can essentially simplify right. So that part is fairly straightforward so if you have time I will just give you an intuition into that otherwise you can work it out easily. Now the first part is one that requires some work right. So this is what we will do for every phase l in the median elimination algorithm we have the probability. So this requires

### [00:13:48](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=828s)

a little bit of thought, so what I am saying so what is this, this is the true best arm at level l right. So at level 1 I would expect this to be a star right. So, the true best arm I am not talking about the capital Q right I am talking about the q stars here, so I am talking about the true best arm right. So in this case I would expect the true this this should be q star a star right in level 1, but in level 2 itself it could be something different because I might have lost a star in the first round itself right. What I am saying is okay this is the best I could have done in the lth round right potentially right, and what is this, this is the best I could have done in the l plus 1 th round right. So the bad case is when this is less than that, right that means I have eliminated

### [00:14:53](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=893s)

some high-ranking arms well all I have left are low ranking arms right. So the bad case is when this quantity is less than that quantity right by how much it should be less right, that is the question that is the trick we are asking here. So if I add an epsilon to this so essentially I have my, hmm, I dont know, let us call this j star right that is the maximum in the lth level. So I have my q star j star here and I have my q star i star here which is the guy that gives me the max here right. If I add an epsilon to this if I add an epsilon to this and this is within that that means this is epsilon optimal when you can consider against that right, do you see that if I add

### [00:15:57](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=957s)

an epsilon to this lower value and the higher value is actually less than that then it is an acceptable situation, because the lower value is within epsilon of the higher value correct, so this is a good outcome. So I am saying the probability of the good outcome is at least 1 minus delta l that means the probability is high okay, does it make sense the probability of the good outcome is at least 1 minus delta okay. Now the thing to notice here is this is not truly epsilon, this is epsilon l right and this is not delta, this is delta l, so why is that the case because every round I will lose epsilon l, right at most epsilon l right. So at the end of the day I should not have lost more than epsilon right. So what I am going to show you is that every round I will lose epsilon l and my epsilon l is chosen such that even if i lose the epsilon l for every l, overall loss will be epsilon right.

### [00:17:00](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1020s)

So that because we know that when the S, in S1 the best number is a star right. And if the overall loss is less than epsilon, then at the end of this I will have at least 1 epsilon optimal arm left okay, so that is basically what we are trying to show here. So this relation makes sense why we are trying to show this okay. And likewise this 1 minus delta l is there because at the end of the day if all the events hold true also my probability must be at least 1 minus delta right. Therefore, we use delta l and that is the reason your epsilon 1 and delta 1 are already smaller than epsilon and delta, because if I start off with epsilon here and delta here I am gone okay. So people know what wlog means right, without loss of generality I am going

### [00:18:06](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1086s)

to consider l equal to one right. So whatever results I show here will will hold for the subsequent l right. So we start off by looking at the first, the event E1 which is first thing I am looking at it I am grossly under estimating the true value right. I mean this should now start looking familiar to you, because in everything we have been doing

### [00:19:10](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1150s)

the same thing we start off by say okay, first thing that has to go wrong is I grossly underestimate the true optimal actions value. And then we will think about okay what happens if I overestimate the sub optimal actions value but I start off by say okay grossly underestimate this right. So now what is the probability of this, and we already have our magic number here, so substitute everything and tell me, so you have the expression here right and you have the magic number there. Right this guy will get cancelled out, again do you have a 4 problem there yeah yeah so

### [00:20:22](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1222s)

well the square should be outside I mean I am just writing it down from the algorithm here, so their results are wrong right. So it should be epsilon l squared by two not epsilon l by two the whole squared and this is a one-sided bound. So the outside 2 will not be there, right so everything will simplify and you will get delta 1 by 3 right. Okay, this is the first event. Suppose it does not hold okay, suppose E1 does not hold

### [00:21:29](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1289s)

essentially I have not made a bad mistake under estimating the best arm right. And since it is maybe I should have done it slightly differently I have said without loss of generality consider l equal to one, but then I put in a star here which actually violates the without loss of generality part okay. So the a star here is actually the best arm left at level l that is how we should think of it, it is not the overall based arm, whatever be the level l it is the best arm left at level l and for l equal to 1 it happens to be a star, the true a star right for l equal to 2 , 3 and 4 this will essentially become the best arm at that level. So I will just put a l there so that you know what I mean okay. This is the best arm in the lth level that is left among all the arms that is left the true best arm in the lth

### [00:22:29](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1349s)

level okay. So next I am going to look at the probability that, hmm, this one I should

### [00:23:39](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1419s)

put the 2 in the numerator is it what do you need for it to cancel out. Epsilon1 by 2, so epsilon1 by 4 no yeah, so this is epsilon by 2 so substitute that I get epsilon squared by four, right that will become half so that is 1 by epsilon squared by 2 so I will get that things are all fine okay good. So I am going to look at this problem

### [00:24:59](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1499s)

right, so sorry not this, so E1 does not hold that means that this is kept true right. So E1 is the event where I have underestimated this so I am saying E1 does not hold that means that it is no longer an underestimate. So this is my estimate is within epsilon by 2 right, but then I am looking at the possibility that yeah, so with my some jth arm which is not epsilon1 optimal right. So that is a condition, no, right I know that my current estimate in the lth round I am going to decide about

### [00:26:09](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1569s)

eliminating in the lth round right in the current round I am not underestimated my a star l okay. So I am within epsilon of that with epsilon1 by 2 of the true a star value right, but then I take some other arm j which is a bad arm, bad in the sense j is not epsilon l close to a star, it is a bad arm right. And I figure out what is the probability that the Q estimate for that arm will be greater than the Q estimate for the a star right. So if this happens right, then there is a chance that a star will get eliminated only a chance right, why it has to be in the lower half not just get beaten by one guy but it has to be in the lower half of the arms right. So I need at least K by two or whatever the size of S l by 2 bad arms to beat me correct, for me to eliminate this arm.

### [00:27:18](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1638s)

Right I need at least half of the arms to beat me not just one arm right, but before we go to that part, so what is the probability of this happening. Well so this conditioning tells us that Q l a star is not too bad right. So what does that mean Q l j has to be more than epsilon by 2 so you remember that figure we drew right. So either this has to be under estimate, well I erased the figure, but either the a star has to be underestimated by more than epsilon by 2 or the a prime has to be over-estimated by more than epsilon by 2 right, here we are conditioning it on the event that a star is not underestimated by more than epsilon by 2. Therefore, j has to be over-estimated by more than epsilon by 2.

### [00:28:19](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1699s)

Right since this event we have conditioned it as false, so that event has to be true okay. So what do we get in that case same thing here right, so I am kind of skipping a step here but people are all fine with that right, I am skipping, rewriting this bound right. So essentially you will have to now replace this with over estimating by epsilon by 2 right. In fact I should probably just make you write that missing step as a homework. So that I am sure that people are all comfortable with the notation nothing more the notation can get really complex, otherwise the concepts are very simple, that is why I am taking so much time talking over it and if I could just write the proof and leave it at that because

### [00:29:23](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1763s)

it is fairly easy, these things are fairly easy. So this is for one arm right and like this I have K arms right, so the probability hmm good. So let now use the same symbols here, I do not agree with, let hash bad be the number of bad arms okay, hash bad be the number of bad arms such that this this condition holds right hash bad be the number of bad arms such that, that condition holds. So these are the number of bad arms that are beating the best arm.

### [00:31:20](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1880s)

So what will that expectation be? Mod S l by 2..yeah, not really but I agree with the mod S l part but not S l by 2 I have a probability for that happening right. And how many such experiments I actually its mod S l minus 1 right potentially everything other than the best arm could be a bad arm right maximum thing is S l minus 1 right. And so it is S l minus 1 into delta1 by 3, so that is the probability of one arm being

### [00:32:22](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=1942s)

bad, one arm actually for which this first relation holds for one bad arm and there are S l minus 1, I am just making it S l to make our life easier. So S l such bad arms so the expected number of bad arms will be S l into delta1 by 3. Now I want to look at the probability that hash bad... this is where we are going to use the Markov inequality right.

### [00:33:30](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2010s)

So I have already written the expectation here, so I am asking you the probability of X greater than equal to a is the expected value of X divided by a right, so this is less than or equal to the expected value which is, divided by a okay. So what have you shown there is that if E1 does not hold if I am good in my estimate for the best arm okay, the probability that half the I mean, so many bad arms will beat me is bounded by 2 delta1 by 3 right. But I am also considering E1 as a bad event right E1 is also bad because my estimate for

### [00:34:36](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2076s)

the best arm is really bad you know. So all bets are off in some sense right because I do not really, I cannot really identify my best term because it is so bad right, so all bets are off so E1 is also bad event right all of this is bad and E1 is also bad. So what is the total probability of something bad happening, the two together, but they are you plug this in if you want to use a fancy term we use the Union bound and then we say the probability of something bad happening is bounded by delta1 right. So this bad is delta1 by 3, that bad is 2 delta1 by 3 and this is actually the complementary event of E1 in fact I can just add the probabilities, I do not really need the Union bound. So the total probability of something of bad happening is delta1 right. So that is essentially

### [00:35:41](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2141s)

what we are started off by saying here. So the probability of good is 1 minus delta now we have shown that the probability of bad is delta l, so the probability of good is 1 minus delta l okay. Great. So one of the nice things about the median elimination algorithm is that it was one of the earliest papers to introduce this kind of a round based algorithms to the bandit literature right. Now a lot of later improvements on both regret based case and people trying to play around with the the pac guarantees all have switched to some kind of round based ideas, you know so you do a certain number of pulls and then you eliminate a certain number of arms right, and then go back and pull the remaining arm some more and then eliminate some more arms. So this kind of a round based elimination methods have become very popular in the bandit

### [00:36:42](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2202s)

literature and the median elimination is one of the earliest such round based elimination approaches then after this it became very popular and a lot of papers started being written using this kind of a round based idea right. So we have so far what we have shown is that it is have you shown that it is pac hmm.. what is it that is fine that ..that I have already spoken about this lemma is taken as proved right, this lemma is taken as proved, so yeah you have to still use the Union bound for every round that I am eliminating right, so what we have to show is well I have all these deltas right, so we have to keep adding them up to make sure that eventually you are less than overall you are less than delta right.

### [00:37:47](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2267s)

So every round the probability of failure is bounded by delta1 right so for the K rounds the probability of failure is I mean whatever the log K rounds the probability of failure is bounded by summing it up. So delta by 2, delta by 4, delta by 8 and so on so forth until you reach 1 right, so that is the summation and or not until you reach 1, until you reach log K rounds. So you will get delta by 2 power logK okay, and the summation of that will go to delta right it is essentially delta into half plus one fourth plus one eighth right .. if that sum runs to infinity you will get one, but the sum is not running to infinity it stops at some finite time, so it will be less than 1, so the summation will be less than delta

### [00:38:50](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2330s)

proved right. So some probability of something bad happening will be less than delta. So likewise you can show these same things for the epsilon right, so at every level you drop utmost by epsilon l right. So the total you would have dropped is epsilon by 4 plus so it is essentially one-fourth plus what is it three-fourth into one or epsilon by 4 into one plus one-fourth and so on so forth right. Three by four l minus 1 yeah yeah that is also upper bounded by 1 if you run it to infinity no its not..yeah it is upper bounded by one if you run that summation to infinity but you are stopping at some finite amount so it will be less than epsilon okay. So both of that are satisfied that is easy enough, the harder, the trickier part is to show the

### [00:39:52](https://www.youtube.com/watch?v=3iNaR0Mq1ug&t=2392s)

sample complexity right. It is not hard, it is just algebra can you let you guys do it or you want me to do the sample complexity part of the proof as well no is it.. depends..somebody say depends, depends on what that is a paper yeah it is there in the paper..it is there in the paper you can look at it. And so I will stop it here for the pac the pac complexity will come back to all of this regret and pac and everything when we look at the full RL problem at some point. Now right now for the bandits we will stop here. IIT Madras Production Funded by Department of Higher Education Ministry of Human Resource Development Government of India www.nptel.ac.in Copyrights Reserved
