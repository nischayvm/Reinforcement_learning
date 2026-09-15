# 24. Value Iteration

- Playlist position: 24 of 60 (selected range: 1–34)
- Video: [Value Iteration](https://www.youtube.com/watch?v=F3DjpixO1bY)
- Caption source: English — NPTEL Verified
- Raw captions: [24_F3DjpixO1bY.en-6UJrWS5jR_I.vtt](raw/24_F3DjpixO1bY.en-6UJrWS5jR_I.vtt)

## Transcript

### [00:00:13](https://www.youtube.com/watch?v=F3DjpixO1bY&t=13s)

So here is a value iteration theorem can read all of it I apologize I go can't go down my

### [00:02:54](https://www.youtube.com/watch?v=F3DjpixO1bY&t=174s)

hand writing seriously detoriates at which this condition in 3 is met for all N greater than capital in okay so pi defined by step four is epsilon optimal and v n plus one minus v star is less than or equal to epsilon by 2 when 3 holds so when this holds v n plus one is epsilon by 2 close to v star right so what is it A and B of kind of easy we already seen that A and B as essentially Banach's fixed point theorem right. I am sorry yeah the Banach fixed point theorem gives us A and B correct what is the difference between C and D why do I have two of these things so they look contradict they look contradictory not order it per say but we did not anyone gives me the right answer I will give you

### [00:04:03](https://www.youtube.com/watch?v=F3DjpixO1bY&t=243s)

a bonus mark that essentially which have been following whatever I have been saying so far so further we will have to take down the roll number and note down that now I got their attention to people who do not know the class averages for my wishes tend to be in like 2 or 3 out of 20 or 50 it does not matter what the denominator is does not seemed to change but so every mark matters so tell me what is the difference why do I need C and D sorry this ? optimal means it is if you say it in a different way then you will get it so what I am saying is that v pi minus v star is less than ? here I am saying v n

### [00:05:11](https://www.youtube.com/watch?v=F3DjpixO1bY&t=311s)

plus minus v star is less than epsilon by two . Remember my space V does not necessarily contain only value functions it is just a space of functions right v n plus one need not be the value function corresponding to the policy pi even though I recover pi by being greedy with respect to v n plus 1 does not mean if I actually solve for value of pi if I find V pi it need not be v n plus 1 right so what three is telling me is that v pi is epsilon not what C is telling me is v pi epsilon optimal what D is telling me is that v n plus 1 epsilon by 2 optimal okay so fun let me give you the work how about you enough I never offered them before right. This is this is on offer nobody took it that is easy enough right all you need to do is just mean following the multiple times I kept saying that V is not the space of value function

### [00:06:14](https://www.youtube.com/watch?v=F3DjpixO1bY&t=374s)

is the very beginning when somebody said V is a space of value function I corrected you of this class very beginning of this class anyway so let us look at the proof well A and B are immediate the follower banach fixed point theorem so we will start off with C and D right so just assume that 3 is made for some n okay so n it is already met that

### [00:07:37](https://www.youtube.com/watch?v=F3DjpixO1bY&t=457s)

condition has been met right and that V p the p has been derived from doing this the p has been derived from doing this. And now I can use my triangle inequality right it does not matter that then this actually does not matter right whether these conditions are met or not I can take an arbitrary v pi and a V star and I can use a triangle inequality and write this because it is just about three points in space right we talked about how I can keep using the triangle inequality in an arbitrary fashion because all I am talking about are just some 3 points in space it so happens that one of them is V pi other one is V n plus 1 the third one is v star but this will hold regardless of which three points I pick okay. So here is a tricky thing I want you to look at so let us look at L pi say I want Lpi to act on V n plus 1 right I want Lpi to act on v

### [00:08:50](https://www.youtube.com/watch?v=F3DjpixO1bY&t=530s)

n plus 1 right so what will be Lpi acting on Vn plus 1 is it space of what Lpi is a an operator corresponding to the bellman equation for pi right sort of way I said last class we left off by saying l pi is a contraction so that Lpi so Lpiis just a bellman value equation operating on Vn plus 1 so what would that be will be this right this but instead of argmax here I will have a summation over p Sa say a summation over pi Sa but what I have done here by pi itself is an argmax a right just one action.

### [00:09:50](https://www.youtube.com/watch?v=F3DjpixO1bY&t=590s)

So if you remember I told you about the deterministic policy is right so this whole thing will go I will just replace this with pi of s is this will be expected value of R given S, pi of s probability of s' given s,pi of s v n plus 1 of s dash so that will essentially be the Lpi acting on v n plus 1 right is it clear this is L pi on v n plus 1 I just read it out I just write in unit known as mnemonic expected value of R given s, pi of s + gamma

### [00:10:53](https://www.youtube.com/watch?v=F3DjpixO1bY&t=653s)

times summation over s' probability of s' given pi of s x v n plus 1 s' okay so now thing that you have to notice how would I get to this pi of s is by using max I use the max operator over this right. So if I had done L on v n plus 1 what would I have obtained L on Vn plus 1 is essentially this right nice right this is this is what this one L or Vn plus 1is essentially this right so what I have done here because I chose my pi to be the max action here so whether

### [00:11:58](https://www.youtube.com/watch?v=F3DjpixO1bY&t=718s)

I apply Lpi on Vn plus 1 or whether I apply L on Vn plus 1 it is the same because the p was chosen to be the max action right so I can say that this is equal to sorry so the two are equal that makes it easier. (Refer Slide Time: 12:24) Now we are going to start simplifying stuff. (Refer Slide Time: 12:27) So I am going to take this expression I am going to try and simplify that

### [00:13:02](https://www.youtube.com/watch?v=F3DjpixO1bY&t=782s)

okay we can I can replace v pi with ?^?l pi v pi done right v pi is a fixed point nothing will change I can just replace it to the Lpi now so can I do this same application of the triangle inequality as we had before so three points are L pi v pi, Vn plus 1 and LVn plus 1 so LVn plus 1 is just another point in space between three points I can write this triangle inequality so this is less than or equal to H this is equal to

### [00:14:23](https://www.youtube.com/watch?v=F3DjpixO1bY&t=863s)

right so this is the reduction we talked about here so from LV I went to L?_p? LV n plus 1 I wen L pi v n plus 1 and from v n plus 1 I went to L V nbecause that is how Vn plus 1 was generated by applying L on VL okay so I have written that. (Refer Slide Time: 15:06) Now I can simplify this so I have V pi n plus 1here v pi minus v n plus 1 here sorry and v pi minus v n plus 1here so I can take it to that side simplify things so I will just get okay that is just

### [00:15:49](https://www.youtube.com/watch?v=F3DjpixO1bY&t=949s)

the first term now we have to simplify the second term what is the second term. (Refer Slide Time: 16:07) I just like we did earlier I have done a repeated application of the triangle inequality is

### [00:16:56](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1016s)

only tricky thing here is a summation goes to infinity because only when I repeat this till infinity will go to v star right but that is fine because this is anyway it is a vanishing quantity as we go along right so this of this sum will actually okay exist

### [00:18:15](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1095s)

limit of a summation yeah well I am you can think of this as V star minus v n plus 1 right because I am just talking about the norm right so as V star minus v n plus 1 and then I have written this up okay. So this is v n plus 1 that is v n plus 2then v n plus 2 v n plus 3 blah this one so forth so what will this be you only said it to be a limit of a summation right guys I need to take 1 gamma out okay so what do we have so we have the first component is less than equal

### [00:19:18](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1158s)

to norm of v square minus v n plus 1less then equal to gamma upon 1 minus gamma intonorm of v n plus 1 minus v n right but when 3 holds what is v n plus 1 minus v n 1 minus gamma upon 2 gamma right so if I plug that then what will I get epsilon by 2 to plug it in there what will I get epsilon by 2 so I have few components here so v pi minus v star is less than or equal to epsilon by plus epsilon by 2 which is epsilon right v pi minus v star is less than or equal to okay when we have actually to complete the proof we have to do that but I am asking you to do that what was the other thing that we wanted to show D or later right. So D essentially was to show that v n plus 1will be at least epsilon by 2 close so we

### [00:20:20](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1220s)

already done so we substitute that here so we get epsilon by 2 so is that so VN - sorry v n plus minus v star is less than or equal to epsilon by 2and what we are showing there is v pi minus v star is less than or equal to epsilon like so that is basically done so we have shown this theorem so essentially what we have here is that value iteration converges with that stopping criterion it converges to a epsilon optimal policy so you have to pick an epsioln first remember gamma comes as part of the problem definition. So once you pick an epsilon you can find a stopping criterion using that expression there and you are all set okay so there is one other very interesting thing that people talk about from a theoretical analysis of algorithms for solving these kinds of MDPs right so it is called the rate of convergence so I have shown you that it converges so there is a whole concept called rate of convergence right how quickly does it approached right so I

### [00:21:23](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1283s)

am not going to get into a huge discussions on rate of convergence and like I mentioned with the deterministic policy thing I actually put up a small right upon rate of convergence as well you can read it. One thing which I want to tell you is that so you can with a little bit of not much right so L is a contraction mapping L is a contraction so at every iteration right so my so what is the contraction factor for L we did this gamma right so for every iteration I can show that my iterates that is basically

### [00:22:24](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1344s)

I start off with v0 then I become take me one then V2 V3 and so on so forth every iteration I can so that the successive iterates will become gamma closer to v star right. So I have some so v1 was some x close to v star then v2 will be gamma X closer to so gamma is small it will converge faster if gamam is very large it will converse lower right so this is called linear convergence with the rate of gamam right so if it falls as gamma square then it will be quadratic convergence right so but linear convergence with the rate of gamam so this is essentially the thing so the interesting aspects I mean if you want to get into the more into the theory of all of these things is to start studying the rates of convergence of different algorithms and so on so forth which I am not going to get into but there is something for as an aside so that you can look at it. IIT Madras Production Funded by Department of Higher Education

### [00:23:25](https://www.youtube.com/watch?v=F3DjpixO1bY&t=1405s)

Ministry of Human Resource Development Government of India www.nptel.ac.in Copyrights Reserved
