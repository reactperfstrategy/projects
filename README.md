# About React Performance Strategies

When Amin and I were were working at a major home entertainment company, we realised that performance of the React front end was overlooked.  It was simply a case of "It will be dealt with later".  This is common -- and in fact makes sense in an Agile world where you need to show the business function on a regular basis.

However, there does come a time when performance does become important -- and sometimes, it is extremly difficult to fix given that the focus was function first.

Some things are easy to fix -- if you know what to look for and employ well known best pratcies.  Some aren't and requre more major surgery!

What we hope to do in this project is to share with you some simple -- and some not so simple -- tips, example and documentaiton on how to start to address your performance issues.

Yes, as Facebook says, React is fast out of the box... but you don't use it out of the box, you add your own components, implement your take on design patterns and so on.  And when things get slow?  What do you do?  Where do you start?

**Measure, measure, and measure again.**  But.... but what are your standards for response time?  Do you have any?  It needs to be objective.  So set some standards.  Login time should be "x", longer transaction times (i.e. when you need to acuire data from several data sources) should be "y".  Set these standards and measure.

If your company has no response time standards.. then there will never be a problem.  This isn't a let off.... It's a bad practice.

## Do you measure?

We used functional testing tools such as TestCafe which is ES6 based.. simple to set up and easy to learn.  This allows you to understand what the user is actually seeing - and provides you an opportunity to *prove* that your app is within standards, or after impotremvemts, how you changes now bring your app into compliant response standards.

## Lesson 2

But... let's say you know in your Customer Contact 'page' response time is far below what it should be.  Where do you really start?

# Summary

And this is what this project is all about.  After you realise you have an issue, where do you start.  WHat changes can you make...

But.... if you measure first, then it sets you up for success.  Remove the objectivity.

Once we get really started, please explore the sub-projects we will create.  Each has example and documentation and actual **proof** of the benefits

We will also (hopefully) introduce some very different approaches to this using the new React Profiler and using Babel to inject performance capturing code.  If we don't get to that -- apologies -- but we have plenty of ideas around it.  So always feel free to share and collaborate with us.



