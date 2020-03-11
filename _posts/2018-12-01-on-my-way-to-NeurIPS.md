---
title: "On My Way to the NeurIPS conference"
date: 2018-12-01
author: frederik
permalink: /posts/2018/12/on-my-way
tags:
  - NeurIPS
  - Conference
location: "Montreal, Canada"
---
I am currently on my way to the NeurIPS'18 conference and I am so excited. 
I am really looking forward to see a lot of presentations of cool work. My
expectations is that there will be so much good inspiration on what directions
to look regarding my own work.

# My Plan
I discussed with my supervisor prof. [Ira Assent](http://users-cs.au.dk/ira/)
what the strategy is for such a conference. Obviously, the strategy is different
depending on what your reasons are for being there in the first place. For me,
there are two main reasons. First, I want to broaden my horizon within the field of
machine learning. Second, I hope to establish some connections to some people
who would be interesting to work with in the future. Maybe I can even find a
good place to go when I am going to study abroad.

During the discussions with Ira, my expectations of what I would be doing at 
the conference changed dramatically. I remember this one thing that she said, 
that changed my perspective quite dramatically:

> You may never get back to talking to someone interesting again, but you can
> always just read the paper associated with the presentation you expected to
> go to.

At first, I thought that my main focus would be to get around to as many interesting
talks as possible. To be honest, I didn't really think that I would be socializing 
that much. Of course, it is a natural thing to ask questions to presentations but I
never thought of using questions as a way to try to "connect" with people with the
intention of establishing relations. It does, however, make a lot of sence to do so. 

Having relation establishment in mind, my plan for the conference is going to be
along the following lines. First of all, I am going to dig through as many
interesting abstracts as possible before I get off the last plane in Montreal. That
way, I will hopefully be better suited for selection which presentations to go for.
In the abstracs, I am going to look for a couple of different things that if find
to have relevance:

1. I will look for research related to my own research, i.e., research related to
	 explainable deep learning. These articles will have
	 the main priority, as they can maybe help me establish relations to future 
	 work partners.
2. I will also look for research that is related to exact solutions to ML problems
	 and speeding up computations as these topics also have my attention and a great
	 potential.
3. Completely new directions may also be interesting.

When I have read through abstracts and found interesting articles. I will start from
the most interesting article and the skim through it. That way, I can prepare 
questions for the authors to ask at the conference. I believe that relevant questions
will be the best way to open a conversation.

When I then go to the conference, I will try to write notes to the presentations that
I go to. I will post the most interesting articles in the [Articles](/articles.html) 
section. 

# The elevator pitch
Another really important point that Ira mentioned, was that it is a good idea
to be able to give a _short_, _medium_, and a _long_ presentation of the work
that I am currenctly doing. I guess that it is a good idea to first try to describe
it in text here. 

#### The short version
I am studying how to identify the _signal_ from particular inputs, that made a given
neural network produce particular predictions. This can, for example, be done by 
decomposing the prediction layer by layer onto the input space. Such signals are of
particluar interest in high stake domains like health care.

#### The medium version
I am studying how to identify the _signal_ from the _noise_ in a particular input, that made a given
neural network make a particular prediction. This can, for example, be done by 
decomposing the prediction layer by layer onto the input space using knowledge about
how the activation of each neuron varies with its input. Such signals are of
particluar interest in high stake domains like health care, self-driving cars or other
decisions about individuals, where it is essential to be able to validate the predictions 
of neural networks.

#### The long version
I am studying how to identify what features a neural network are looking for when
it makes its predictions. More specifically, i am trying to separate the actual
_signal_ from the noise in the input. This can, for example, be done by learning
how the activations of each neuron varies with its input in order to decompose
a prediction back through the neurons (like a gradient) but only projecting the
prediction through the "relevant" connections.

Being ablo to extract the signal from the input is of high relevance in high stake 
domains like health care, finance, or self-driving cars, where it is quint essential
to be able to validate predictions in order to avoid unwanted consequences from 
"networks going wild". 

Another direction whithin this area is to refine signals already extracted signals
by including global knowledge. Global knowledge could be ideas like "similar features"
should have similar importance in the signals.

Now, I just need to practice this a lot. Also I might need to reiterate over these
three descriptions a couple of times in order to make them really good. 

That was it for this first blog post. Now I just need to get started reading all the
titles and abstracts. 
