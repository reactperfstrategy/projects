# About React Performance Strategies

When we were were working at a major home entertainment company in London, we realised that performance of the React front end was overlooked.  It was simply a case of "It will be dealt with later".  This is common -- and in fact makes sense in an Agile world where you need to show the business function on a regular basis.

However, there does come a time when performance does become important -- and sometimes, it is extremly difficult to fix given that the focus was function first and not using well understood React 'patterns'.  

Some things are easy to fix -- if you know what to look for and employ well known best practices.  Some aren't and require major surgery!

What we hope to do in this project is to share with you some simple -- and some not so simple -- tips, examples and documentation on how to start to address your performance issues.

Yes, as Facebook says, React is fast out of the box... but you don't use it out of the box; you add your own components, implement your take on design patterns and so on.  And when things get slow?  What do you do?  Where do you start?

First, **Measure, measure, and measure again.**  

But.... but what are your company's standards for response time?  Do they have any?  It needs to be objective.  So set some standards.  Login time should be "x", longer transaction times (i.e. when you need to acquire data from several data sources) should be "y".  Set these standards and measure.

If your company has no response time standards.. then there will never be a problem.  This isn't a let off.... It's a bad practice.

As an aside, if your company does not have standards in this area, try and impress upon them that the business will use their subjective views to make things uncomfortable.  Or... try and impress upon them what response times should be...

1. Login < 2 seconds
1. Navigation < 1 second
1. Acquiring data (Simple < 2 seconds -- We recognise that the above might conflict with this)
1. Cancelling out of dialogues -- Immediate (This is here because of poorly designed behaviour causing Redux store changes that require data re-acquisition on a cancel.)  Remember what we said about... just do it... then fix later? That is wrong. Do it right first.

For longer running transactions, always put up a Spinner.  Did you know that a Spinner convinces the user that your app is 10% quicker?

**General rule** -- If you know that a transaction is of the non-trivial variety, put up a Spinner.  (Non-Trivial transactions should be more than +2-3 seconds).  This is based on our human attention span -- which is only about 2 seconds.  After that, we start looking 'elsewhere'.  This underlines the importance of 'snappy' response time.  Keep your users focused, and engaged.  When they expect a longer response, let them know by a Spinner.  

Understand human behaviour.  Understand a blink of an eye is 300ms (or so).  There are plenty of sites that discuss this -- in a biological sense.  [One of them.](https://uxdesign.cc/5-lessons-from-biology-that-predict-successful-ux-products-of-the-future-7492ffead5bf) Makes sense?

## Do you measure?

We used functional testing tools such as [TestCafe](https://devexpress.github.io/testcafe/) which is ES6 based.. simple to set up and easy to learn.  This allows you to understand what the user is actually seeing - and provides you an opportunity to *prove* that your app is within standards, or after improvements, how your changes bring your app into compliant response standards.

But... let's say you know in your Customer Contact 'page' response time is far below where it should be.  Where do you really start?

# Summary

And this is what this project is all about.  After you realise you have an issue, where do you start.  What changes can you make?

But... if you measure first, then it sets you up for success.  Remove the objectivity. Prove you have brought value.

Once we get really started, please explore the sub-projects we will create.  Each has examples and documentation and actual **proof** of the benefits

We will also (hopefully) introduce some very different approaches to this using the new React Profiler and using Babel to inject performance capturing code.  If we don't get to that -- apologies -- but we have plenty of ideas around it.  So always feel free to share and collaborate with us.



