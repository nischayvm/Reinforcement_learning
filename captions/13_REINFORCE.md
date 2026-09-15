# 13. REINFORCE

- Playlist position: 13 of 60 (selected range: 1–34)
- Video: [REINFORCE](https://www.youtube.com/watch?v=WIBWQ7lOXoA)
- Caption source: English — NPTEL Verified
- Raw captions: [13_WIBWQ7lOXoA.en-6UJrWS5jR_I.vtt](raw/13_WIBWQ7lOXoA.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:20](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=20s)

Let us denote the set of parameters by theta so I am going to come up with some kind of a performance measure for a specific choice of theta, so I will call it eta of theta right so for what does the specific choice of theta correspond to, suppose my theta is like composed of theta1 theta2... thetaK so I give you values for theta1 theta2 theta3... theta K so what does this correspond to ONE policy when I say I am looking at a specific value for theta it corresponds to one policy. So when I say eta of theta that means I am evaluating that policy somehow okay so what is the most natural evaluation measure you can think of for a policy, expected pay off, right expected the expected payoff is the evaluation for the policy so yes I am going to do I am going to do that there okay, so what is the expected payoff you know what

### [00:01:23](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=83s)

the expected payoff is, this is the expected payoff I will get for taking action a. This is a probability that I will take action a when I am selecting actions according to theta right right so this is a standard notation I do not know if people are familiar with this, this means pi is a function that is parameterized by theta right and whatever specific value I give for theta will define what that pi is okay and then this means it is going to take some other argument okay, so this is the input to the function okay. Which is defined by these parameters theta okay so this is how I, when you put a semicolon here that means it is parameterized form okay, so essentially since pi a semicolon theta

### [00:02:40](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=160s)

means that is the policy defined by the current settings of parameters theta times the q star a right because q star a is the true expectation for taking arm a right and then sum over all a, I will basically get the expected reward but if I am having a deterministic policy that means essentially only one arm I will take all the other arms of probability 0 then the payoff will be q star of that arm right okay, so now once I have this kind of a performance measure so what do I do is essentially I take theta. Right I take theta, I find the gradient of the performance okay so where the gradient is taken with respect to theta right so I look at how the performance changes with changing theta and I will try to move theta in the direction of the increase in the performance,

### [00:03:46](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=226s)

okay. So this is called gradient ascent so people might have heard about gradient descent earlier so this is gradient descent, so I am going up the gradient, right. If the performance improves if I change theta in some direction then I will change my theta in that direction, okay does that make sense people see this or do you need more pictorial analogies, so let us say that I have one parameter theta, I have one parameter theta right and that is eta of theta, let us say this is my is this a good way to do it, right let us

### [00:04:47](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=287s)

say that I have my performance whatever is an acceptable range of theta so my performance goes like this right. So I initially start off with some guess for theta right that will be my initial guess for theta right then what I do, I measure this and then I compute the gradient right so the gradient is there so if I look at which direction I should move my theta, essentially I should move in this direction so I move a little bit and set that as theta1 okay then I measure the gradient again okay still I have to move in this direction more so I keep doing that and I think I will declare that I have reached the highest performance there. So this is essentially how I do it okay there are a couple of questions which you might

### [00:05:47](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=347s)

ask me here, why do I have to do this in this kind of an incremental fashion why cannot I just take the derivative of that and find the highest point and settle down there, sorry I do not have the function at all so forget about closed form, I do not have the function at all what is that function that is q star of a times pi right I know pi but I do not know q star. If I know q star my problem is solved right, I do not need to do any of these things, that function itself I do not know right. So how am I evaluating this function and trying to find the gradient, by sampling so I am pulling a lot of arms right according to my current policy pi right and then I am trying to evaluate the policy pi and then trying to find the gradient at that point right, so because everything is done through sampling. So whatever gradient I compute at this point will not be the correct gradient right this

### [00:06:50](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=410s)

is too simple I mean it has to be either that direction or this direction, this is too simple right but think of a multi dimensional case when there are many many parameters, the right direction you will have to compute can get messed up right so instead of going in all the parameters instead of identifying the right direction some parameters you might get the right direction some parameters you will get the wrong direction and so on so forth right. Therefore every time you make only small steps because if we tried if we say oh I have computed the direction of the gradient I will just keep moving in that direction until my.. or I will take a huge step in the direction until my performance drops or something that would not work because the direction itself might be wrong so in this case I mean we have always moved in the right direction every step. It is possible that because you are estimating the gradient you might actually make the wrong computation and move in the wrong direction sometimes okay so what really you can hope for from these kinds of methods which are called stochastic gradient approaches okay

### [00:07:52](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=472s)

they are called stochastic gradient approaches because you do not know the true gradient and every time you make an estimate of what the true gradient will be and then you are using that for making moves. I mean the most popular form of this will be called SGD which is stochastic gradient descent okay it is a very popular optimization technique nowadays but in this case you are using stochastic gradient ascent but still it is the same stochastic gradient idea and so you have to be careful about how you use it and the best that you can hope to get is that in an expected sense over many many updates right. I did I did now I showed you two updates so if you make this update says this kind of updates many times in an expected sense you will move in the right direction of the gradient right so that is the kind of guarantee that typically you expect for these kinds of methods okay, so is it clear now is clearer now if people are not hundred percent clear about what I am talking just stop and ask right I can elaborate at the risk of slowing down

### [00:08:55](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=535s)

yeah. Good point yeah so we will come to that so we are going to talk about that, so we do not know the function itself right how are you going to estimate the gradient right, so we will come to that in a minute so we know we have a functional form for this now I am going to write down the gradient for this expression right this is the expression we have, I am going to write down the gradient for this expression. Okay so this is assuming that q star of a because it is a parameter of the problem right it has nothing to do with the policy right as far as your policy parameterization is

### [00:10:00](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=600s)

concerned q star is a constant right because it is a it is something to do with the problem so I can I do not have to do this I just have to differentiate this with respect to theta right, so now I am going to do some hand waving. So what did I do here, I multiplied and divided by pi, okay. So for this to work what do I need, pi is non zero for all a so this is one condition that you need for all of this any kind of pi that you assume okay has to be nonzero for all a it has to assume some nonzero probability, now if you think about this particular expression

### [00:11:07](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=667s)

right I will put a bracket around that right so what does this remind you off, does it look like an expectation computation I am looking at the expected value of some function right. Where I am taking samples according to probability pi, right this looks like an expected value right, I am summing over all possible outcomes of A all possible values here right that is the probability so I am essentially taking the expectation taken according to pi of... is it fine right. So everybody on board with that right so that I can write that expectation

### [00:12:21](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=741s)

oh okay sorry about the font, so the expectation is taken with respect to pi, okay. Is it clear? so now we know how to make an estimate of the expectations right how do you do that we draw sample and then take an average right so we can do that so essentially what I am going to do is pull an arm that is a sample right when you say draw a sample according to pi that essentially means I have to pull an arm and what happens when I pull an arm, I get a reward right but the reward does not figure in here. The expectation of the reward directly figures in here right so I can actually write this

### [00:13:25](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=805s)

as a double expectation you know mean the expectation is taken over not only pi but also over the process that generates the reward q star right it is also the process that generates the reward so my sample here is going to consist of Rt right is it clear I mean this is a very subtle thing, people are here with me on this is it clear. See q star itself is already an expectation right so instead of because I do not know this expectation I will have to estimate this expectation as well and that can be done by just taking the Rt so what I will do now is at every time t I will sample an arm, I will pull the arm figure out what the reward is right but is that sufficient, no I have to do this right I just cannot use the Rt directly I will have to use this also right. So I will take the gradient of pi, evaluated at A divided by the.. so this is my one sample

### [00:14:36](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=876s)

right this is because the expectation I am taking is of this quantity so the sample that I draw is actually this right and I have to do this over I do not know some number n, pi a t you are right, is it fine , no no no I am not using t I am sorry, I promised you that I will use n for discrete time and t for continuous time. So we are talking about discrete times here it has to be n I do not know if i used t here, sorry about that but all of you a erase in your notebook that t and write down n, for

### [00:15:43](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=943s)

this part of, sorry about that right so this is clear is there anything missing right, so I need to have 1 by n there so this gives me the gradient right so this is fine oh are we still okay, we are not because this is actually a estimation okay. So I cannot put equal to there, it is only an approximation great so can we compute this, we can right because we know pi we are the ones who determine what pi should be right

### [00:16:43](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1003s)

because at the beginning I choose a parameterized representation that I can choose whatever suppose it is softmax well I know how to take the derivative of soft max right or if it is a continuous action I can just use a say a Gaussian right I know how to take the derivative of a Gaussian with respect to its parameters right. Or if it is a multinomial what do I do you know how to take the derivative of a multinomial as well right so the derivative is very simple so I know what form of the function I choose it so I can go ahead and take the derivative, there are a couple of reasons for it so estimating q star need not always be the right thing to do okay because I have not

### [00:17:49](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1069s)

introduced all the complications I am hesitating whether I should go there or not. But the thing is so the q star function sometimes turns out to be incredibly complex okay as a function of the state space okay not necessarily here right as a function of the state space q turns out to be incredibly complex whereas a direct representation of the policy turns out to be a lot more simple right for example there are many inventory control problems where the policy essentially turns out to be if the inventory is below a certain level you buy, if the inventory is above a certain level you do not buy okay. But then the value function itself becomes a very complicated function of how many of the items are left of different types and so on so forth so the function itself becomes a lot harder to learn so there are instances like this where this is easier to learn right and there are a couple of other cases especially when you are talking about very large problems

### [00:18:50](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1130s)

for example we will see that policy gradient approaches generalize very easily to problems with continuous actions. So where there are individual actions so if you are talking about value function methods right where I typically store a value for each action now I am going to have continuous actions it is not clear how to handle it there are ways of handling it but it turns out that they are not that well behaved as policy gradient approaches are when the action space is continuous right so there are many reasons why you want to consider continuous actions I mean policy gradient methods. Primarily I would say the, one of the primary motivations is to handle continuous actions, okay. So this is some kind of a batch update, hmm because the expectation is taken with

### [00:20:00](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1200s)

respect to the pi, yeah you could do more simplifications of that if you want to right but what is your question again, yeah but I need to take this expectation with respect to the sample the probability distribution pi right. So and I cannot separate this I cannot write this out as some I really cannot simplify this further because my q star is here right so this is the expectation of this whole quantity so I really cannot split this apart and say that okay I will just simplify this expectation and take only the expected value of q star a, can I, I cannot take E of AB is not A into

### [00:21:01](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1261s)

E of B is it if A is only a constant right not otherwise I am not sure whether we can simplify this further right. So what we are doing here is some kind of a batch mode so if you think of how we are doing this sampling so I am taking some theta fixing it pulling the arms multiple times right fixing theta pulling arms capital n times and then taking this average right and then what computing the gradient and then using that to change the parameters right this is one way of doing it another way of doing it to say that okay I will have a theta I will pull an arm I will compute the gradient. And I will change the parameters right so you can have a some kind of an incremental version.

### [00:22:11](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1331s)

So where I am saying at every step I will change my parameters by some fraction delta t, I will do this at every step right sorry and so this is what I am doing so what I am essentially will end up doing is theta will be theta plus delta theta, theta n +1 will be theta n plus delta theta n right I will do this

### [00:23:14](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1394s)

at every time, every time I pull an arm I will change this right I mean that is essentially the gradient of the ln it turns out this simplifies your life a lot this observation simplifies your life a lot when you are trying to actually solve the solve problems later right now you can immediately think of soft max becoming very easy to differentiate we have now taken log and there is lots of exponents there right. So all the e power thing will vanish so it will become lot easier to differentiate for you right so what I am going to do now is to include another term here rather arbitrarily

### [00:24:37](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1477s)

called bn which we refer to as the reinforcement baseline, right and adding the bn should not affect the whole process that is what the bn should not really be a function of a, yeah theta basically so it should not be a function of the action I take right. If it is a function of the action I take then it becomes dependent on theta so as long as it is not a function of the action I take I can keep adding a I can add this thing it is called the reinforcement baseline right so one way of thinking about it is I am when I get a reward right I do not know if the reward is a good reward or a bad reward so giving a baseline and saying that if you are above this baseline it is a good reward if you are below this baseline it is a bad reward okay. kind of allows you to calibrate the rewards right one typical way in which this reinforcement base line is used is to just take the average of all the rewards I have obtained so far

### [00:25:38](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1538s)

right this is all the rewards regardless of which arm I play I keep accumulating the rewards right now when I play a particular arm if it is above this average then it is a good arm if it is below this average then it is a bad arm right. So valid after, yeah..hmm fine.. eventually it will eventually it will be all fine right so initially you might be making some mistakes because the initial few the b will be wrong right so you might actually think a good arm is bad and a bad arm is good I mean depending but eventually it will all work out does not matter right so if you think about if the reward is good right then I will go in the direction of the gradient right but if the reward is bad then I will go in the opposite direction of the gradient right.

### [00:26:39](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1599s)

So in some sense that is a little waving here that but then it is fine it turns out that adding the reinforcement baseline makes the convergence behavior of this algorithm a little more stable okay but it is not necessary you can if you are going to implement this you can do it without the reinforcement baseline also right so this is called the and this term is sometimes called the called the characteristic eligibility. So what is the characteristic eligibility it essentially tells you, if you

### [00:27:43](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1663s)

do that then you get into actor critic I will talk about that later, I will talk about that later yeah sure yeah you could do that right and that is essentially one of the motivations for getting into actor critic algorithms, so that requires you to maintain q star estimates as well as the pi estimates as well as the pi representation. So the pi would be the critic and the q star would be the actor,uff.. other way around the pi would be the actor the q star will be the critic so that is another class of algorithms right which address some of the drawbacks of policy gradient approaches right I will talk about it but somewhere halfway down the course not now so after this I am going to go back and start talking about the full RL problem and at some point I will come back and do actor critic yeah. So his question was why do I use Rn right why cannot I plug-in q there right you could and yeah and typically when you do that it performs better the algorithm it is actually

### [00:28:50](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1730s)

a it reduces variants significantly at the cost of adding significant bias right there are other issues you know you well you know what are the other issues going to actor critic but I will talk about it later right and going back. So why is that called the characteristic eligibility so if you think about it so it essentially chooses which of the thetas are most responsible for a change at that point right so that is the term that determines that is the term that is the theta dependent term in your updates right and it tells you which theta is more responsible for change that is happening here there suppose there are three or four different parameters that I have right. So whichever has the highest gradient whichever direction you have the highest gradient that is the direction where the largest change is going to happen right, so it is essentially

### [00:29:52](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1792s)

this telling you which theta is more eligible to receive the update that is why it is called the characteristic eligibility right did that make sense to people I think i have lost more people today than in the previous classes no great. So this whole thing right this way of doing this incremental version of doing this update is actually called the called the reinforce algorithm, first proposed by this guy called Williams in 98, Williams proposed reinforce in I think in 1988 and in fact he proposed this in the context of neural networks right so he when he came up with this algorithm neural networks were still ruling right.

### [00:30:55](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1855s)

So he proposed this in the context of neural networks he said that your thetas are weights of a neural network right and then he came up with this update and then the biggest contribution he did was he said that hey this looks like a really crazy update right I mean how is this going to work and initially people are very skeptical he actually showed that in an expected sense right even though I am doing this update after just pulling one arm in an expected sense the gradient will be in the right direction right. If I repeat this experiment multiple times and I watch how the weights evolve right they will actually move in the same direction as it would have happened if I had computed the correct gradient and then taken steps in that direction so essentially he established that for this reinforce update and it since then it has kind of been the one sole hope of convergence for all kinds of complex function approximations and RL okay. So it works really well but it is extreme extremely slow, reinforce is extremely slow

### [00:32:02](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1922s)

because the variance is very high so when I want to move on from this I will talk about the other problems of reinforce here is a horrible part about the paper so reinforce is actually an acronym there is an expansion each letter stands actually for a word he came up with a name for the algorithm which actually shortened to reinforce. And then that started the trend for convoluted names in the RL community okay anyone knows what the expansion of reinforce is do you know what the expansion of reinforce is, forgot okay, I cannot for the life of me I refuse to memorize what reinforce stands for, great so let us do some special cases of reinforce right I want to consider a binary bandit.

### [00:33:05](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=1985s)

Or let us say I take a bandit with two actions okay but they can have arbitrary rewards okay here is the parameterization I choose this is essentially the Bernoulli thing right so I have two actions with some probability theta I will select action 1,1-theta I will select

### [00:34:06](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2046s)

action 0 okay so what do I need to do now to get that update rule we have to find doe ln pi by doe theta so what this will be, it will be 1 if a is 1, it will be minus 1 if correct. No!! yeah look at ln pi right it is not doe pi by doe theta, it is doe ln pi by doe theta yeah so it will be 1 by theta if a is one and it will be minus 1 by 1 minus theta if a is zero right, we can write it like that, substitute a is 1, so 1 minus theta and 1

### [00:35:16](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2116s)

minus theta will get cancelled out you will get 1 by theta. Substitute a is zero, theta and theta will get cancelled out, you will get minus 1 by 1 minus theta okay a very compact way of writing it and now I am going to say that I will choose my alpha to be some rho times theta into 1 minus theta. So it turns out that as long as your alpha is not dependent on the actual reward that you get okay it can be dependent on the theta this is what William showed as long is not dependent on the actual reward you are all fine okay you will converge so that is essentially this is result so I can make it dependent on my theta it should not be dependent on the actual action you sample okay and the actual reward that you receive so as long

### [00:36:18](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2178s)

as that is there it is fine all right. And I am going to choose my b to be 0, why am I making this specific choices so now I let me plug everything back in so what does my delta theta look like, so alpha n which is rho into theta into 1 minus theta into Rn minus bn which is 0 so it is Rn into doe ln this which will be a minus theta by theta into 1 minus theta right so what do I end up getting rho okay so what is the what is the interpretation for this, let us say I take action one okay and I get a reward of 1. So what do I get, rho into 1 minus theta that is how much I change my value by so which

### [00:37:25](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2245s)

is essentially this right rho into 1 minus theta right suppose I took action but what about I took action one right and my reward was one right what will I do for 0 oh there is no there is only one parameter right it is automatically my other parameter will get adjusted because it is 1 minus theta suppose I took action one and got a reward of 0 what happens no change. Suppose I took action of 0 and got a reward of 1 what happens, minus theta into Rn right so that is essentially what I have here right so this is minus theta into Rn right so theta is my pi t a t if you remember right and then this R so that is essentially what I have, so this is this is what L R-I right so essentially L R-I is a is a gradient following algorithm

### [00:38:38](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2318s)

actually it is a reinforce algorithm right so you can try to look at different choices for the alphas and the different choices for pi right and try to come up with this kind of update rules right. We will do the soft max action selection as I described in the previous class right so do that right where I replace all my qs with some arbitrary theta suppose I have K actions or K arms then I will have theta1 to theta K these are my parameters and the probability of selecting arm I will be e power theta I by beta divided by summation over j e power theta j by beta right so this is my softmax expression so derive my reinforce update rules assuming that is the expression, right that is one I am going to give you another homework.

### [00:39:41](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2381s)

The same thing, I said one of the nice things about doing reinforce. Is that it allows us to handle continuous actions right allows us to handle continuous actions, actions need not be discrete so far we have been looking at the cases where actions are discrete so I am going to use, that as my probability distribution that is my policy

### [00:40:44](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2444s)

okay give me the reinforce update rules so how many rules will I have for reinforce update rules here 2 - one for the mu, one for the sigma right. Get me the reinforce update rules and yeah so try to simplify as much as possible because when you do the ln mu, I mean the ln pi derivatives will get all kinds of weird constants coming there so you can choose your alpha appropriately so that some of these constants get cancelled out so that I can have just like we did here right I chose my rho to be theta into 1 minus theta likewise you can choose your constants in this case also right the alphas to be something

### [00:41:44](https://www.youtube.com/watch?v=WIBWQ7lOXoA&t=2504s)

different so that you end up with a good nice-looking form okay great. IIT Madras Production Funded by Department of Higher Education Ministry of Human Resource Development Government of India www.nptel.ac.in Copyrights Reserved
