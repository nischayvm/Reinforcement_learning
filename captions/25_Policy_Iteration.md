# 25. Policy Iteration

- Playlist position: 25 of 60 (selected range: 1–34)
- Video: [Policy Iteration](https://www.youtube.com/watch?v=09L0nqw9Vnc)
- Caption source: English — NPTEL Official
- Raw captions: [25_09L0nqw9Vnc.en-LUU0EuDKgKo.vtt](raw/25_09L0nqw9Vnc.en-LUU0EuDKgKo.vtt)

## Transcript

### [00:00:13](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=13s)

So we need to do policy iteration so shall we are, should we not when we started late I know it's my mistake here oh okay, so that leaves us with 15 minutes I think, we could do it in 15 minutes, so policy ration the idea is very simple, right so I start off with some arbitrary policy let us say p0 may start off with some arbitrary policy p0 I find weep I not, right then what do, I do I be greedy with respect to vp0 I will find

### [00:01:22](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=82s)

p1 right. . So being greedy is this right so I will take some p0 solve fine vp0, right then do this and I will find p1, right and then I find vp1 plug that backend here right, so essentially I will plug in VN here find pn+1 right, so keep going until I converge and convergence here is more straight forward if you stay with the same policy you converge where unusually convergence is much faster the rate of convergence much faster with policy, iteration but, for variety of reasons value iteration remains a very favorite algorithm for many war people don’t like policy iterations for, some reasons. So but people get the idea for the policy iteration is right you can go implement policy patients rather easy, right so first so let's

### [00:02:27](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=147s)

of arbitrary sorry I hate going back and forth select an arbitrary p0, right second step is called, policy evaluation so where you say, refined vp0 right so policy evaluation

### [00:03:28](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=208s)

is just find vpn right so we can just do this by solving the system of equations I can just take the inverter inversion in the inverse of that matrix and solve it right or if you like it you could do the iterative fashion just just like you did in value iteration instead of iterating on L I can iterate on lp, right and then I let have some stopping criterion for stopping it but I can do this as well next thing is called policy. . Policy improvement okay this is a second step is called policy evaluation third step is called policy improvement, just like we mentioned

### [00:04:46](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=286s)

earlier it says mark Maxes then component-wise, right for every state yes you do the max, it is whatever I wrote here before erased it at the beginning at exactly that, only difference is here I am plugging in vpn it is not V* right so this vpn and I do this argmax over p and at every step because I am checking for equality for stopping right. So there could be multiple actions that give you the max here right, so if at step n you chose an action for giving a max like step n there is some action your chosen as policy for a state s in step n+1 if the same action belongs to the max set you will pick that actually you do not pick an arbitrary action from the maxim, suppose let us say going up and going right right both are optimal, right but in the previous step I had chosen going up for the state this step I should chose I should choose going up also in otherwise

### [00:05:49](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=349s)

I will just keep oscillating between up and right up and right I might not figure out that I have stopped right. So I shouldn't choose an action from the maximizes randomly right are arbitrarily I have to have some mechanism by which I consistently break ties so that, policies do not change when they do not have to, pn+1 =pn stop and declare that pn is 5* otherwise go too, well otherwise increment n and go to step 2, right so it’s rather easy, right so if the stopping condition holds can you see why pn should be p*, that

### [00:07:07](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=427s)

doesn't mean anything it just means it’s a fixed point, ypn should be p* well it is a fixed point but it is a fixed point of L. If you think about it max over p rp+?ppvp ray that operation that looks like L that is yell operating on vp then if I get that p in the same beep I same p again, right so that means the value function hasn't changed, right so that means V=lv, so that means it is the optimal value function right so if pn=pn+1, because of the way I am generating the sequence of p and if pn=pn+ 1 then pn is p*, also I haven’t changed right because the apology has it changes the value function will interchange fiesta no because of the way we are generating here right remain so.

### [00:08:08](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=488s)

So if the value function hasn’t changed and this is essentially this part of it is essentially L operating on vp and it does not change so that essentially means, that it is the optimal value function, okay and what else do we need to show I said if pn=pn+1 then pn is V* pn is a p* by the way right ,what else we have to show, that I have to show that happens right I will have to show that that happens so we will do that in two ways one we will have to show that so vpn+1 = vpn, right.

### [00:09:11](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=551s)

So why is that why you think that will be greater, so basically pn+1 is a greedy policy according to be pn, okay so taken vpn and action greedily with respect to it and I get pn+1, so that is what I mean like pn+1 satisfy 3 then, right this is clear right so because

### [00:10:29](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=629s)

pn+1 satisfies 3 so that is being greedy with respect to vn well pn is some arbitrary policy which is the same as this then that will give the same answer otherwise this will be greater, because this is the one obtained by maximizing this expression, wait I took this expression I am maximizing it and whatever gives me the maximum I am saying is pn+1, right. So this is the maximum on the left hand side so the maximum has to be greater than or equal to whatever value I will get by plugging in some other pn here because this is the max okay this is clear right one more step, so I can say so why can I say this because this is actually equal to vn that the right hand side will be equal to vpn because it's a fixed

### [00:11:45](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=705s)

point of lp, so this is lp operating the lpn operating on vpn such a fixed-point so this is vpn so essentially this is it and if I multiply both sides by, what do I get so that into this is what, right. So every step I will keep improving okay so the last bit we need is to show that, there are only a finite number of policies that you can search through, if you are having a finite MDP finite number of deterministic policies we are searching through only deterministic policies here, only finite a number of deterministic policies you can search through if you have a finite MDP so that is basic approved it so policy iteration will converge, but every time I have to become better and there are

### [00:12:47](https://www.youtube.com/watch?v=09L0nqw9Vnc&t=767s)

only finite number of things I can search through at some point so I 'll have to stop, or is it okay the component ways so every component, of v is greater than sorry I didn't define it earlier I should have so this essentially means set vn+1 of s1 is greater than or equal to v1 of s1 of s2 s3 for all s, right I think there are people clamoring to come in so that's why I stopped we can go out and you can ask questions.
