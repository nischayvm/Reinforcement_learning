# 18. Bellman Equation

- Playlist position: 18 of 60 (selected range: 1–34)
- Video: [Bellman Equation](https://www.youtube.com/watch?v=CTPHADvQxSs)
- Caption source: English — NPTEL Verified
- Raw captions: [18_CTPHADvQxSs.en-6UJrWS5jR_I.vtt](raw/18_CTPHADvQxSs.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:01](https://www.youtube.com/watch?v=CTPHADvQxSs&t=1s)

So we are talking about value functions okay people remember value functions so we defined value functions we said V pi of S equal to expected value of pi right. And then we defined Q pi

### [00:01:18](https://www.youtube.com/watch?v=CTPHADvQxSs&t=78s)

right good, so now we are going to start unrolling their expectation and so people remember this expression right so all of you are clear about it so I don't have to explain what is happening there again right so V pi of s is means starting in state s following policy pi . Thereafter and taking the expectations of the, the returns that I am getting I am going to start unrolling this right so what does it what does it look like so i am going to say V pi of s equal to, yes

### [00:02:30](https://www.youtube.com/watch?v=CTPHADvQxSs&t=150s)

What can I write here, I GT plus s1 right but what is what would be the value of GT plus for the expected value of GT+1. V pi of whatever state you land up in right so let us go I am going to say that this is equal to V pi of s prime were s prime is the state I am going to add up and we will quantify s prime in a minute right so, so people agree with me on this right is s prime is the state I go to from s right so I can take this summation and write it like this. Everybody onboard okay great so now I need a slight slight of hand here right so I took GT and then I wrote

### [00:03:34](https://www.youtube.com/watch?v=CTPHADvQxSs&t=214s)

it as one term plus the expected value of GT but that is fine because I am anyway going to take a expectation eventually right so this is slight reordering of the expectations right instead of taking an expectation of the full expression. I took the expectation of the inner one alone but one thing you have to remember is it is only a partial expectation because s prime can change right so for me to get the full expectation I need to condition on s prime also That is why this expression is still inside the expectation so if this has been the full expectation I could have taking it out, out of the expectation since it is still only partially conditioned so I need to conditioned on the full thing okay so now I have to write it out so that will get rid of the expectations okay so one way of writing out this expectation is to think of it like a generative process okay. So remember what did I say we are going to do we'll start in state s right then select

### [00:04:38](https://www.youtube.com/watch?v=CTPHADvQxSs&t=278s)

actions according to policy pi right and measure the, expected return right so you are starting in state is and the selecting actions according to policy pi. So what does that mean using pi right and I am selecting actions according to policy pi so let us say I pick some action a right so now what I am going to do I am going to get some reward corresponding to that RT plus yeah the RT plus 1 will give me something that corresponds to that reward so but then before I can find out what RT plud 1 this I need to specify what the next state is going to be so I need this. So taken action a then okay I determine what s prime is and then I determine

### [00:05:42](https://www.youtube.com/watch?v=CTPHADvQxSs&t=342s)

What but I already determined what s prime is it so I can do this right so this is one step I am taking a pick an action a according to pi right now that is going to cause a transition to some s Prime according to this P that we have there right and once I know what the S prime is I can figure out what the expected reward will be as well as V pi s prime because I know what s prime is is so what is the probability that this will be my return is this times the probability I will pick action a so this whole thing gives me the probability that this will be my expected return okay so now i have to do this overall

### [00:06:51](https://www.youtube.com/watch?v=CTPHADvQxSs&t=411s)

all possible outcomes. So basically a sum over s prime okay is it clear how we got this right this one right so I have a s a right that I picked a a first then I pick an s Prime according to p now I have a SA S prime right so what I need to do is figure out what this expectation of RT plus 1 would be right so that is given in my MDP right the expectation of RT plus 1 would be given SA S prime what is the reward so that is this expectation I've written it here expectation of r given SAS prime right and then the future is gamma v pi s prime so that S Prime has already been fixed so I can just add the gamma v pi s prime here. So the probability that this will be the outcome right is the probability of s prime given S and A time's the probability of picking A given S .

### [00:07:53](https://www.youtube.com/watch?v=CTPHADvQxSs&t=473s)

So all these things put together gives me the probability that this will be the outcome right so that is the expected outcome for one choice of A and one choice of S prime so I'll have to sum this overall choices of S prime and all choices of A for me to get the overall expectation so that is essentially what I've done here summed over x prime summed over a . This is nice right so we written V pi in terms of V pi. So this, this system of it is a system of equations right you can see there is a system of equations that you have one equation for every, every state how many variables are there number of as many variables as there

### [00:08:56](https://www.youtube.com/watch?v=CTPHADvQxSs&t=536s)

are number of states the number of states is not the variable that is also fixed as many variables as number of states and what is a very we here V pi of s is the variable. So essentially so instead of thinking of it as a function now I can think of it as a collection of variables right one for each state right and I have N such equations and N such variables and can I solve it. Depends on what, its linear N variables N equations so when can you not solve it yeah then, then then yeah so when we get dependent columns and so it becomes redundant so you have multiple solutions and sorts of three so it turns out as I'll show you in the next class right the system of equations have a unique solution always right

### [00:10:05](https://www.youtube.com/watch?v=CTPHADvQxSs&t=605s)

by virtue of the fact that the P that you are using is stochastic so the rows of that P matrix will sum to one right so by virtue of that fact we can actually go back and show that there will be a unique solution I will just need to write, write is slightly different in a different notation for us to see that so I will do that in the next class right so this is pretty much has a unique solution and this is sometimes known as The Bellman Equation for V pi after the Richard Bellman who's one of the pioneers in the field of stochastic dynamic programming okay. Like ways you can write a bellman equation for Q pi okay. Anyone wants to tell me about the bellman equation for Q pi would be

### [00:11:14](https://www.youtube.com/watch?v=CTPHADvQxSs&t=674s)

No think of it in the generative process right so what is the first thing you do when you're thinking about Q pi SA .They start with yes I pick a right I mean it is fixed so there is no summing over there right it's S and A is picked right so what do I have to sum over next only the s primes because this pi a s is out of the picture here right because I have already picked A right . So I do not need to I do not need to sample from pi they already pick case so I just start my summing over s prime. Right now, now SA is prime are all fixed right so I can write expected value of R given SA s prime plus gamma times. Now the interesting question is what goes there I could write V pi and it will be perfectly correct but I will not be writing Q pi in terms of Q pi.

### [00:12:26](https://www.youtube.com/watch?v=CTPHADvQxSs&t=746s)

Summation over all actions This is the Bellman Equation for Q pi okay. So this should also give you one, one more ancillary equation there which is. And that is the way Q and V are related and what about Q pi can you write Q pi in terms

### [00:13:39](https://www.youtube.com/watch?v=CTPHADvQxSs&t=819s)

of V pi. That's exactly what the earlier equation was the Bellman Equation substitute the last summation with V pi and that is essentially Q pi in terms of V pi. Right so I cannot write Q pi S a in terms of V pi s so it has to be in terms of V pi of the subsequent state right but V pi is I can write in terms of Q pi oops sorry.
