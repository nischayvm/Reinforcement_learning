# 07. Concentration Bounds

- Playlist position: 7 of 60 (selected range: 1–34)
- Video: [Concentration Bounds](https://www.youtube.com/watch?v=KB-ZDvLbuOQ)
- Caption source: English — NPTEL Verified
- Raw captions: [07_KB-ZDvLbuOQ.en-6UJrWS5jR_I.vtt](raw/07_KB-ZDvLbuOQ.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:18](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=18s)

So this is interesting because we can have a nice theorem which says that, so this particular form of UCB is actually called UCB 1 right, and in the literature if you generally see UCB without any qualifier assigned to it, it usually means UCB1 okay, there are many many variants on it we are not going to look at all the variants there is like normal UCB then UCB Revisited, UCB Improved, UCB2 right so, there are many many variations of UCB right and each one gives you a slightly better theoretical results than the one that I am going to write down right, and sometimes involving exponentially harder analysis. UCB1 is fairly trivial compared to the other algorithms that were proposed later and I

### [00:01:24](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=84s)

just want to give you a flavor of the kind of work that is done in this area right, so I am NOT going to get into the other things but we will certainly put all those papers up on Moodle, if people want to read they can read those okay. Another thing about UCB1 is that we can have arbitrary reward distributions so, some of the other algorithms that are out there assume say Bernoulli rewards right for showing their results and so on so forth the right thing about UCB 1 is arbitrary reward.

### [00:04:21](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=261s)

So capital delta i is Q star a star minus Q star i essentially this means the loss that you will incur if you play i, the expected loss that you will incur if you play i instead of playing a star, right you remember what a star is, the max over a of Q star a right so, that is a star, argmax a of Q star a is a star right so I will always denote by a star the optimal action right so, what does this tell you, so the regret right is upper bounded by eight times ln n by delta I, the summation running over all the non optimal arms ,why all the non optimal arms? Because delta I is 0 for optimal arm, so I do not really want that to figure in the summation okay, plus 1 plus pi squared by 3 that is the magic constant okay, times summation over all j delta j right.

### [00:05:23](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=323s)

And here i am being little sloppy i have to exclude the optimal arm here also but i do not because it is 0 anyway, delta j 0 anyway so, I mean symmetrically just as I have this summation here I should have the summation there, but I can be a little sloppy and I can write it like that because, i do not have to worry about the additional 0 terms I'm adding okay, great. How did we get from here to there or more importantly how do we get this expression? Right so before we go on so I want to introduce a little bit of notation here

### [00:06:24](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=384s)

that's the term that tells you the number of times it is a random variable that represents the number of times I have played arm i in the first n trials okay. Number of times I have played arm i in the first n trials does it make sense, so then i can write my regret after n trials as summation over i expected value of that times delta i, people get that so the expected, the regret that I expect to have after n time steps is

### [00:07:25](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=445s)

I will take each action, look at the number of times I would have played that action till that time right, multiply it by the regret of playing that action right. So if I played the optimal action then the regret is 0,so if I play some sub optimal action then I will be adding that delta i times, the number of times I have played that sub optimal action i right. So this is essentially my definition of regret so I have now a formal way of writing down my definition of regret, is this is clear, any questions? Okay. so one more notation is one thing which I yeah so one more notation that I will have here, it is a random variable that denotes the reward that I obtained for playing action i at time n, some n okay some

### [00:08:26](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=506s)

arbitrary n, time n if I play action i right what is the reward that I get right? since we are assuming everything is stationary right so the expectation of this will be, this will tell me if people are following it or not, so what is X i n the reward I get for playing arm i at time n right what is the expected value of that somebody say something. One of you put your hand up and say something, so that i can, its very hard for me to make out in that murmur hand hand hand, Q star of i, people see why since we are assuming

### [00:09:30](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=570s)

things are stationary this expectation is really not going to depend on n, so then it becomes expected reward I get for pulling arm i which is essentially Q star i okay, great. So anything else that I need to do notation wise so, essentially to show this result right, what I am going to try and show is that, this guy is bounded and I am going to show that that guy is bounded so what I am going to show? We're going to show that

### [00:10:33](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=633s)

the expected value of T j of n or T i of n is bounded by 8 by delta j squared ln n so, since i multiply by another delta here to get the regret so that will get me the first term in the regret and some constant here which will get me the second term in the regret. It's not calculated at the nth stage it's calculated by using their true values that's Q star you do not know the values but it's just a definition its just a quantity, that's the expected regret that you are going to get for playing arm i, its the expected loss you would accrue for playing arm i. If I had played the best arm over and over again right, if I played the best term over and over again I would get Q star a star if I play arm i, I am going to get Q star i right,

### [00:11:36](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=696s)

so the loss i am going to get is Q star a star minus Q star i correct, so this is what I am denoting by delta i this is the loss that I expect to accrue for playing arm i, just playing with that one arm right and if I keep playing that arm repeatedly the total loss i am going to accrue is delta i a times the number of times i will play i right and I sum this over all the arms. So one of these arms in the summation or one or more of these arms I mean we do not know one or more of these arms in the summation would be optimal. And for those terms delta i will be 0, so the regret, the contribution to the regret will be 0 and all the other sub optimal arms will contribute delta i to the regret. Yeah. Because I am assuming the reward distributions are stationary, right you remember I said

### [00:12:36](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=756s)

you are deciding the reward by tossing a coin but you do not change the coin right because you do not change the coin does not matter when I toss the coin the probability of it coming up heads will be the same whether I toss it the first time or whether toss it at the tenth time I pull the arm, the probability of it coming heads will be the same and that is the expectation, right so the expectation will be the same right. so one way to think about the this expectation is right so, I do multiple experiments right I do several experiments every time starting from time 0 right, I do i do like millions of experiments okay every time I start from time 0 and I keep pulling arms for some number of time steps right and then i reset my whole system start from time 0 and pull for another say 100 time steps or something like that right when i do this experiments like this in the 10th time step if I pull arm three right so in this million experiments some number of times I would have pulled arm three in the 10th time step okay, then I'll take

### [00:13:37](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=817s)

all the rewards I saw then I'll take the average of that right that is one way of thinking about what this expectation means. So now you understand right it does not matter whether I pulled arm three at the 10th time step or whether I pull arm three at the thousandth time step if i take this expectation across these million trials, it will be the same. So that is essentially what we're saying here okay, is it is it clear so what we are trying to show is this right so if you are able to show this then we are all done as long as this constant here evaluates to 1 plus pi squared by 3 okay our proof is all done okay. Now we have to now go and start counting that okay, so here things start get getting interesting subho you want to complete the proof okay so before I move on with the proof i will need one more i need one more fact, so

### [00:15:18](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=918s)

they're on this whole set of results in probability theory called concentration inequalities or concentration bounds okay. Or sometimes called large deviation bounds okay, these are essentially results that relate the true expectations of distributions okay, with estimated values of those expectations from samples not just expectations I mean different kinds of statistics you have different bounds you have bounds on expectations you have bounds on variance right and so on so forth, right so essentially the idea behind these bounds is to kind of characterize right so, given a certain number of samples from which you are estimating a statistic right the statistics in this case will for the one that we are interested in is the expectation right. So we are interested in the expectation as a statistic right, so I have some number of samples from which I am estimating this expectation right and I have the true expectations right

### [00:16:23](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=983s)

so as the number of samples increases how quickly or how slowly does this estimation approach my true expectation so this is something that we want to characterize so we will talk about one such bound which is very popular bound which is applied all over the place okay, so if you are going to do anything in machine learning forget about RL anything that has remotely shades of theoretical results in machine learning it's a good idea to know more about concentration bounds but at least the least you should know about is the Chernoff bounds or the Chernoff Hoeffding bounds. So this is a very specialized form of the bound I am writing right very narrow form of the bound that i am writing specifically for this setting that we are interested in

### [00:17:27](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1047s)

right the Chernoff bound is slightly more general than what i am stating now right and so you can look it up I mean so you can look up I don't know your favorite online resource right Wikipedia or whatever mathematica one of those things right so it will give you a more expanded bound. Okay So you can see the setup here I am assuming that X1 to Xn

### [00:18:50](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1130s)

are random variables right each one with a range 0 to 1 right, that is kind of putting it here and if it is not in the range 0 to 1 you will have to do some kind of normalization in the bound right, but for the time being let's just assume it's in the range 0 to 1. And such that the expected value of Xt right given all the variables that came before that is mu and then this holds for all t basically it essentially means that all of the variables have a mean mu, all the variables each one independently X1 is a random variable with mean mu in the range 0 to 1, X2 is a random variable with mean mu in the range 0 to 1 okay. So essentially that is what we are assuming and I am defining another random variable which we call Sn which is essentially summing up all the X1 to Xn and divide by n, okay so you get that. So what I am I trying to estimate us with Sn, mu right I am trying to estimate the mean

### [00:19:58](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1198s)

mu so, one way right now let us try to make this little concrete in our case so, that it becomes easier for you to understand right so X1 to Xn are random variables that are corresponding to different times I have pulled the same arm i right so I have pulled arm i n times right, so every time I pull the arm I am going to get some reward from the range 0 to 1 right, since I am assuming it is a stationary distribution all these rewards will have the same mean mu, correct? And Sn is the average right this Sn is essentially my Q j right if you think about it so, my Q j is like one sample of my random variable Sn, is it clear, what I mean by saying Qj is a sample of Sn because, Sn is a random variable right what is Qj it is one realization of that random variable, because I have taken

### [00:21:03](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1263s)

actual samples and taken the average it is one realization of that random variable right. And what I am going to now tell you is okay given that i have taken n samples so, in our case it will be Nj samples right given that i have taken Nj samples, how can you relate Q j with what how can I relate Q j with Q star j okay, so given that I have taken Nj samples which is my n here how can I relate Q j with Q star j okay. So this is how the hoeffding bound is applicable in our case right so i will write down the expression i am not going to prove it okay, so that will get little bit more involved write down the expression and after that we can apply it in deriving those bonds okay. So essentially what i have here is now the probability that Sn is greater than or equal

### [00:22:10](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1330s)

to mu plus some epsilon, hmm, where did I do a here because a is action right so I don't want to confuse a for action with something else yeah, this is what this is the problem with translating on the fly okay, fine so it should be n or n squared? Subho.. so what

### [00:23:21](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1401s)

does this mean the probability that my Sn will be far away from my mu in one direction, so mu is the true mean, Sn is the estimated mean, the probability that Sn will be greater than at least epsilon from mu right is lesser than e power minus two epsilon squared n right, so the smaller the epsilon , what happen? Smaller the probability or larger the probability larger the probability smaller the epsilon larger the probability right so larger the probability of me making an error, I mean if I want to be really really confident then I need more and more samples right. If I want epsilon to be very small then n has to be very large only then I will get a high probability for it right what about this it says in the other direction probability that the estimate I make will be far away from epsilon, basically below epsilon right

### [00:24:27](https://www.youtube.com/watch?v=KB-ZDvLbuOQ&t=1467s)

is again bounded by the same expression. IIT Madras Production Funded by Department of Higher Education Ministry of Human Resource Development Government of India www.nptel.ac.in Copyrights Reserved
