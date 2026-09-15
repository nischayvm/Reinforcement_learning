# 09. PAC Bounds

- Playlist position: 9 of 60 (selected range: 1–34)
- Video: [PAC Bounds](https://www.youtube.com/watch?v=N_9HgdhXKIY)
- Caption source: English — NPTEL Verified
- Raw captions: [09_N_9HgdhXKIY.en-6UJrWS5jR_I.vtt](raw/09_N_9HgdhXKIY.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:26](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=26s)

Chernoff Hoeffding bound, we saw that already. So that is one result right we looked at it

### [00:01:53](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=113s)

in the last class and you saw how we used it to manage to bound the regret of UCB right so we will be looking at yet another class of bandit algorithms today right so the PAC bandits and we will be using the Chernoff hoeffding bound again to bound a slightly different quantity but nevertheless of interest you remember the Markov inequality Elec people, people who did probability theory one form of writing it is this which is what we will need right assuming a is, a is positive, the expected.

### [00:03:12](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=192s)

So, the x support is in the positive range I mean so I mean whatever makes appropriate sense for you to make sure that this is a probability right next thing you use is the Union bound this is this all of you should know the probability of the union of multiple events right is less than or equal to the sum of the probabilities of the individual events that is rather straightforward it has a fancy name called Union bound right so whenever somebody says oh, hence by Union

### [00:04:13](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=253s)

bound we can write this result essentially all they are saying is that they are upper bounding the probability of the joint event by the sum of the probabilities of the individual events okay these are the results we will just keep using them as we will do some of the proofs today. Okay so we talked about multiple solution concepts for bandit algorithms right so the first one was asymptotic correctness and the second one we talked about was regret optimality which we already looked at one example of a regret optimal algorithm UCB or UCB1 more correctly even though popularly when people say UCB they refer to UCB1 right and then what is the third one pac optimality right which was the probably approximately correct thing where you are trying to bound with some probability right that I mean you are close

### [00:05:15](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=315s)

enough to the true solution right So that is essentially the guarantee that we want to give right. So what we look at today are right so pac bounds for multi-armed bandit problems right I will start off with a very, very simple algorithm start off with a very, very simple algorithm right this is just to get you started right it is not a true algorithm that you have to use, its just to get you started so I have an input which is I will give you an epsilon and a delta and what I am asking for is a guarantee that at the end of this algorithm the arm that I return to you will be epsilon close to the optimal arm with probability 1 minus delta.

### [00:06:19](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=379s)

Right with a very high probability if when this algorithm finishes running with a very high probability I will give you an arm which is epsilon close to the true arm the payoff of the arm that I give you will be epsilon close to the true arm so if you remember the pac guarantee that we wrote right so most pac algorithm pac style algorithms essentially take this epsilon and delta as inputs right and they determine some parameters of the algorithms based on this epsilon and delta okay so I am writing the algorithm in the same style as it is in the paper that we will give you to read so that it is easy for you to map it. Unfortunately I will still do the online translation of notation so that you can compare across multiple algorithms okay, and this paper is way, way better written than the UCB paper

### [00:07:25](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=445s)

okay so it is actually you can understand the paper when you read it okay so this is the on the median elimination algorithm by Eyal Even-Dar, Shie Mannor and Yishay Mansour okay, it is titled Action elimination for Reinforcement Learning okay so the nice thing about this ok I will tell you the nice things about the paper later. But the really nice thing about the paper is it is well written so you can easily read it. very simple algorithm right the algorithm is a very simple algorithm what is the n in

### [00:09:23](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=563s)

the log, where where, what is n inside the log, n is the number of arms right so what did I say I changed it to K right sorry yeah you are right over in the last class, last lecture I changed it to K yeah right this is a very simple algorithm all I am saying is take each arm sample it some number of times okay we can think about it right this is this will work see if I if I get a good enough estimate for each arm right if you get a good enough estimate of the reward of each arm then I can say that with a very high probability I will be epsilon optimal right. So this of course there is always a small chance that I will go wrong right do you see what I am saying here so the idea is very simple so I will take an arm keep pulling it many many times right until I have gotten a good estimate of the of the expectation right so remember the probability with which it is going to come up with 1 or whatever right so whatever is my expectation parameter I will just keep pulling the arm multiple

### [00:10:27](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=627s)

times until I get a good estimate of the expectation I will do that for each of the arms that I have right. And once I have a good enough estimate of the expectation all I have to do is now go and play the arm that has the highest expectation right that is essentially what I am doing here now the magic here is in that number which I have written down there right I mean given K, epsilon and delta that is actually a number okay remember I take epsilon and everything as inputs given all of this is actually a it is actually a number right so that magic number how did I produce somewhere yeah I wrote all of this I wrote all of these things so that you know that you are going to use them to produce that magic number so it is very simple. So let us make things a little formal so we call this algorithm naive, so then algorithm

### [00:12:28](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=748s)

Naive which takes as input epsilon delta is an epsilon delta pac algorithm, you remember what is epsilon delta pac we defined it in the earlier lecture right epsilon delta pac gives you that whatever guarantees you are talking about right epsilon delta pac algorithm with arm sample complexity essentially the number of times you pull the arms given by order of n by epsilon squared into log n by delta right so this part is obvious right I pull each arm 1 by epsilon square times ln K by delta right so for n arms I have to do that n times so my overall sample complexity is this okay, so the interesting part now is to show that it is actually epsilon delta pac whats it obviously yeah for today's lecture

### [00:13:39](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=819s)

if I write n by mistake right please point it out to me. So I will correct it to K right okay so how do we prove it well the sample complexity part is obvious we do not have to prove that we just have to prove the epsilon delta pac so for that we will assume that let a prime be an arm such that q star a prime okay so a prime is an arm which is not epsilon optimal right an arm that is epsilon optimal is epsilon close to the best arm right so q star a star is the reward corresponding

### [00:14:44](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=884s)

to the best arm we know that right so I am saying that I will pick an arm a prime such that it is at least epsilon away from q star a star right. So the q star of a prime is at least epsilon away from q star a star right so that means it is a bad arm right so arms that are more than epsilon close to the true arm I do not care right if I select them I am happy because my guarantee is satisfied I really have to worry about making a mistake which in this case is selecting an arm that is more than epsilon away from the true optimal okay so basically we are looking at the event right so this is what we want we are looking at right so if this is the case then the algorithm will output a prime instead of a star correct.

### [00:15:45](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=945s)

People onboard with me on this right so if Q a prime is greater than Q a star, then my algorithm will output at least it will not output a star for me to select a prime as the best arm at least this condition has to be satisfied okay let us put it that way right for my algorithm to output a prime as the best arm for sure this condition must be satisfied in fact a prime has to be higher than every other arm right only then I will output that but at least this condition has to be satisfied so essentially I am going to look at the probability of this happening all right and then we will try to bound that right. So people can see why we need this condition right so if a prime has to be reported as the best arm it has to be at least better than a star right great so that is the condition

### [00:16:46](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1006s)

so already we are being little loose here okay, this is not really the probability that yes a prime will be the best arm okay but it is only looking at some sub event of that it is not all the events together but this will give me at least a bound on the probability so that is essentially why you are looking at this event okay. Right so what is happening here, let us say that is my

### [00:18:05](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1085s)

that is my q star a star okay that is my right and this gap is at least this gap is at least epsilon, okay so there is this is the setup that we have now so and I am making some estimate of q star a prime which is Q a prime right and I am making some estimate of q star a star which is Q a star so the condition I am asking is that Q prime a prime should be higher than I mean Q a prime should be higher than Q a star right. So essentially I am saying that I should have Q a prime here Q a star somewhere lower right

### [00:19:09](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1149s)

so this is the case I am looking at right so this all automatically means that either Q a prime has to be more than epsilon by two from q star a prime right it should be at least epsilon by more than epsilon by two above or Q a star should be more than epsilon by two below q star a star, right if they are exactly epsilon by two they will be equal I mean they won't be one above the other nights if one is epsilon by two below other is epsilon by two above so you can think of cases where this is actually here right so this could be here in which case q star I mean q star a star has to be even below right it will be more than epsilon away forget about epsilon by two right so likewise for cases where you are overestimating Q a star Then this will also have to be higher than that in which case again it will be more than epsilon away right so the interesting case is when it is in between the two right then

### [00:20:11](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1211s)

it has to at least one of them has to be epsilon by two away from the true estimate right either as a overestimate or as an underestimate right is it clear so why I wrote this down, right one of these two events has to be satisfied. right I am just taking them as independent

### [00:21:23](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1283s)

events and summing them up and that still be an upper bound on the total probability you have right, making things simpler and simpler for me and now what happens here it kind of in the Chernoff space right. So I can apply Chernoff bound here so what would be the case here e power minus two epsilon squared by four into l, yeah so let us do that so this will be less than or equal to e power minus two epsilon squared by four into l, what about the other term, the same right it is a symmetrical bound so if that is plus epsilon by two or minus epsilon by

### [00:22:23](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1343s)

two, it is going to be the same right so is it clear okay so now plug in this l there so what do you get, hmm, so essentially what we need to do now is adjust this l so that

### [00:23:24](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1404s)

all those things get cancelled out that is basically what we are looking for right and you will be left with what should you be left with. What should you be left with what do you think you should be left with no no no I want this probability delta this is the probability of me making a mistake right so it should be delta, should I be left with delta, not quite this is the probability of me choosing one non optimal arm by mistake what if all my arms are non-optimal except the one optimal arm right everything is away from that is the worst case so I should have delta by K or K-1 so we will take delta by K, okay that is easier than and so this whole thing should simplify to delta by K right so that is what I should be looking for so what should be my l right.

### [00:24:28](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1468s)

So this if we plug this in what will I get so the four by epsilon squared will go so I will get 2 ln 2K by delta, that is not quite right and what do I get then, yeah 2 into 2K by delta so I will get delta by K I will get delta by K right is it fine I simplify this I get delta by K so now you know how you actually come up with this magic number l right, by actually deriving this bound and then figuring out what else should I plug in here so that I get the necessary error for the probability okay

### [00:26:22](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1582s)

so that is just for one a prime hmm there is a two outside right, two epsilon okay.

### [00:27:30](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1650s)

So this is clear this is a naive algorithm and the analysis also is pretty simple, pretty straightforward right so all of you are happy with this right so if you if I give you an algorithm with a slightly different way of selecting actions you can all derive the complex the l that is required basically great it turns out that so we have produced this complexity here right it turns out that it is almost impossible to get rid of this 1 by epsilon squared right and log 1 by delta right, so when I try to come up with another pac algorithm right I want to you remember what I said about pac analysis. So I will give you an epsilon delta and now the interesting part is telling me how you can achieve this epsilon delta with as few samples as possible correct so in this case I am telling you that this is the sample complexity right and K figures in two places you have

### [00:28:32](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1712s)

a K by epsilon squared and log K by delta right it turns out that this 1 by epsilon squared and log of 1 by delta is very hard to get rid of right but then people have come up with and can you get rid of this K, it should depend on K why at least once right. I have to try every am at least one so I cannot get rid of the K also right so the only thing I can try and minimize here is well I can try and get rid of this K right so I can try to get rid of the log K dependency right and then have K by epsilon squared log 1 by delta

### [00:29:36](https://www.youtube.com/watch?v=N_9HgdhXKIY&t=1776s)

roughly I can try to move in that direction and once I reach there I will probably be in, left with trying to get rid of this two here right and try to make the 2 into 3 by 2 or 1.77 or something like that. you know how these things proceed right so you can try to optimize the constants but more or less this 1 by epsilon squared and log 1 by delta is something that will have to live with okay. IIT Madras Production Funded by Department of Higher Education Ministry of Human Resource Development Government of India www.nptel.ac.in Copyrights reserved
