# Accessible Web Development
## It’s OK to not know something.

---

## Introduction

* Kate Lynch
  * Senior Application Developer
  * University of Pennsylvania Libraries
  * @fa[envelope] katherly [at] upenn [dot] edu

* Web accessibility researcher and developer
  * WCAG 2.0, 2.1
  * Creating/remediating web-based software and content
  * Accessibility testing with users
  * Techniques for making challenging content accessible

---

## Outline

* What is web accessibility?
* What I wish I had known sooner
* Message of hope

Note:

I have three and a half points I’m going to touch on today.  One half point will go to my definition of web accessibility, how I regard this work and this cause as I’ve learned and taught about it over the years.  Two more will be about what I wish I’d known sooner; the easy stuff and the hard stuff respectively, and finally it is my wish to leave you all with a message of hope about your interest and work in this field.

---

## What is web accessibility?

“Web accessibility means that people with disabilities can use the web.”

-Tim Berners-Lee

---

## What is web accessibility?

* POUR
  * Perceivable
  * Operable
  * Understandable
  * Robust

---

# What I wish I had known sooner: the easy stuff

---

## The "low-hanging fruit"

Note:

There is the concept of “low-hanging fruit” in web accessibility which refers to the easiest things to know you can get right, with the most reward for the end user.  Taking care of these aspects won’t make your sight completely accessible, but if your site doesn’t have a lot of challenging content like drag-and-drop interfaces or custom media viewers, it will take your site a surprising percentage of the way there.

---

## The "low-hanging fruit"

* Image alt text
* Lists
* Properly ordered heading

---

## The "low-hanging fruit"

* Image alt text
  ```html
  <img src=”hospital.jpg” alt=”Pennsylvania Hospital”>
  ```
* Lists
* Properly ordered headings

---

## The "low-hanging fruit"

* Image alt text
* Lists
  ```html
  <ul>
    <li>What is web accessibility?</li>
    <li>What I wish I had known sooner</li>
    <li>Message of hope</li>
  </ul>
```
* Properly ordered heading

---

## The "low-hanging fruit"

* Image alt text
* Lists
* Properly ordered heading
  ```html
  <h1>There Should Be Only One (Much of the Time)</h1>
    <h2>There Can Be More Than One Of Me</h2>
      <h3>Provided That We Occur in Numeric Order</h3>
    <h2>Increasing And Decreasing in Number</h2>
  ```

---

## The "low-hanging fruit"

* Avoid walls of text
* Be mindful of color contrast
* Provide alternatives to rich media
  * Equivalent text
  * Captions, transcription

---

[image]

Note:

All of these things, and just generally properly formed HTML, as well as separation of content from presentation are rewarding techniques for developers and users alike.  It’s like mathematics or other types of programming, as you work out a problem, when things start to make sense, that’s when they start to beautifully express information.

---

## Prioritizing - Must, should, can

---

## Prioritizing - Must, should, can

* What **<span style="color: #FF0000">must</span>** be done?
* What **<span style="color: #FF0000">should</span>** be done?
* What **<span style="color: #FF0000">else can</span>** be done?

Note:

When prioritizing accessibility tasks, create a plan for what to address as soon as possible by asking yourself first:

What MUST be done to make this site accessible, information perceivable and understandable, the interfaces operable so the same actions are acheivable for all users?

After that, what SHOULD be done to make all information truly accessible, ie linking to a textual description of a video is good for baseline accessibility so disabled users have access to the information, but ultimately, we SHOULD include captions in the video to enhance presentation of the information for users who will benefit from captions.

And finally after that, what, if anything else, CAN be done to make the site more accessible?  Are there decorative images that are properly ignored by the screenreader but should really be in the CSS?  Can you cut down on the number of clicks it takes to do something?  Stuff left for the “can” phase should only be stuff that enhances existing accessibility measures taken.  If it’s required, it’s not a “can,” it’s a “must.”

---

## The (actual) user experience

[image]

Note:

And there’s the actual user experience.  That is, we have these guidelines and recommendations, and testing tools available, but we need to avoid teaching to the test.  I’ve seen and made some web interfaces that technically pass validators or meet defined standards, but the user experience is still unnecssarily arduous or just plain opaque.  On some occasions, it’s worthwhile to think harder -- OK, let’s assume I’m a developer with no impairments, how do I use this site?  What is the experience like for me?  What information can I glean?  What’s easy, and what’s hard?  Interface design is its own thing for a reason, because designing interfaces is hard.  We just need to make sure that the easy stuff for users without impairments is easy for all users, and the stuff that’s hard, if we honestly can’t make it easier, at least isn’t harder because a user has an impairment or is operating with assistive tech.

---

## Testing with screen readers

[image]

Note:

Also, learning how to test with screen readers.  When I first started in web development, I was dimly aware that screen readers...existed, and at the time required a separate stylesheet to present a website as all-text.  All-text versions of sites as accessible equivalents have since fallen out of regard as an equivalent experience, but something that I picked up on pretty quickly once I started to take this seriously was that it’s not enough for the website to talk.  You know, you turn on the screen reader, the website talks, it reads all the content on the page, and we’re done, right?  No.  This goes back to putting yourself in the user’s shoes.  Reflecting on how we interact with websites, we don’t read them linearly, like we do a book.  But screen readers do, if we just plug them in and let them talk.  Screen reader users have tools within the software that allow them to more deftly skim a web page and navigate quickly to various sections, and these can only be used if we structure the pages following certain rules, such as implementing headings and lists.  Only by observing screen reader users in person and through services like YouTube, sitting with JAWS and VoiceOver screen readers’ documentation, and operating the software myself did I develop a workflow where I became more confident that I actually knew what I was testing for.

---

## Equivalent, not identical

[image]

Note:

Finally, this is and remains the most important concept I grasped about accessibility as I began to learn.  We strive to make the user experience equivalent for all.  Equivalent doesn’t mean identical.  It means that everyone coming to the site can access and understand the same information, and can perform the same tasks with the same relative ease and efficiency.  Once I understood this, it became far less daunting to contemplate how I might tackle making more complex web content beyond flat HTML and images accessible, because it’s not about “There’s no way to make an inherently visual task such as image editing screen reader accessible!” but rather “what does a screen reader user come to this online image editor for, and how can we facilitate that?”

---

## What I wish I had known earlier: the hard stuff

Note:

And then there’s the hard stuff.  The stuff I’m going to cover isn’t necessarily hard from a technical implementation standpoint, but can be hard to really wrap your head around and know if you’re doing adequately.

---

## Testing beyond screen readers

* [Dyslexic typoglycemia simulation in Javascript](http://geon.github.io/programming/2016/03/03/dsxyliea)
* ["Colorblind" Twitterbot](https://github.com/jakevoytko/colorblind )

Note:

Testing beyond screen readers.  This is a trap that the best of us have fallen into; we test with a screen reader, if the results are good, the page is accessible.  And it’s true that screen reader technologies are some of the toughest customers when it comes to an equivalent user experience, but this tends to lead us to overly focusing on users with visual impairments and forgetting about others.  

Other impairments, particularly those related to fine motor impairments and cognitive or perceptual impairments, are harder to adequately test for without gaining more understanding of what those impairments are like for users on a regular basis.  Getting familiar with the user community and reading documentation like WCAG specifically addressing these impairments is imperative, as is trying to test with users with a variety of perspectives when possible, not just screen reader users.

From this I started developing techniques to simulate what I’ve learned about these varied user experiences.  Turn the mouse around for perceptual, create distractions for yourself (Youtube tabs), use your non-dominant hand on the mouse for fine motor skills.

Really challenge the way you interact with the site and be mindful of how much more work it is to accomplish tasks in your testing and what can be done to cut down on that.

---

## Consider the target audience

* [Glaucoma.org](https://www.glaucoma.org/)
* [News for Betty](http://newsforbetty.com/)
* [IDA Dyslexia handbook (Browsealoud demonstration)](https://dyslexiaida.org/ida-dyslexia-handbook/)

Note:

Consider the target audience.  The target audience of your site will influence what decisions get made in the “must, should, can” phase.  While baseline levels of accessibility need to exist regardless of the target audience, when the target is more likely to include folks with specific accessibility needs, additional considerations that might otherwise fall into the “should” or “can” categories become a must.  I have some examples linked on the slide here.

---

## Prioritizing accessibility in development

* Punch lists, cheat sheets
  * [Penn Libraries' web accessibility documentation](https://upenn-libraries.github.io/Accessibility/)

---

## It's OK to not already know this

Note:

It’s OK to not already know this.  None of this stuff was taught when I earned my degree, and most of the time, it’s still not in any curriculum.  Most often, people come to this after they’ve been doing this a while, and it’s important to shift attitudes to make it safe for developers to work through the process of integrating accessibility in their work.

---

## It's OK to not already know this

* ...and it's OK to make mistakes

Note:

And it’s OK to make mistakes.  Mistakes are proof that you’re trying.  

There’s a lot to learn here, from the basic concepts, to various standards, to testing and validating.  We can regard this process as we regard all other processes of learning in software development.  You need to understand the frameworks, the code syntax, adequate testing methods, and the only way to learn is to try, make mistakes, communicate, and learn.

---

## Conclusion

Note:

So, if this is a bit of a downer, I promised you a message of hope.  So here we are...

---

## You have a gift

* Lead by example
* ...never stop helping someone!
* Embrace continuous improvement

Note:

Working with vendors to address accessibility can be challenging and our pleas for improvement can seem to fall down a rabbit hole of unresolved JIRA tickets, but working with developers and accessibility advocates and testers doesn’t have to be hard.

Accessibility education materials and distribution of knowledge is certainly better than it was 5 years ago but is by no means so distributed that we can assume developers “should” have learned about this by now.  Often people learn about it through venues like this one.  

As an accessibility advocate, use teachable moments to educate and inspire.  Assume accessibility issues you encounter aren’t done out of carelessness, and realize that you, armed with this knowledge, have a gift that you can share with the community.  Embrace real-life agile, real continuous improvement, and never stop educating yourself and helping others craft better user experiences for all.

---

Thank you!

* Katherine Lynch
  * @fa[envelope] katherly [at] upenn [dot] edu

---

## Web accessibility resources - developers

* [Web accessibility best practices](https://upenn-libraries.github.io/Accessibility/)
* [Principles of accessible design](https://webaim.org/intro/#principles)
* [Color contrast checker (online tool)](https://webaim.org/resources/contrastchecker/)
* [WAVE accessibility evaluator (online tool)](https://wave.webaim.org/)
* [WAVE browser extensions](https://wave.webaim.org/extension/)

---

## Web accessibility resources - working with vendors

* [VPAT information and template](https://www.section508.gov/sell/vpat)
* [What is Section 508?](https://www.epa.gov/accessibility/what-section-508)
* [WCAG overview](https://www.w3.org/WAI/standards-guidelines/wcag/)
* [PDF accessibility overview](https://www.adobe.com/accessibility/pdf/pdf-accessibility-overview.html)
* [Temple University’s guide to accessible purchasing](https://accessibility.temple.edu/guide-accessible-purchasing)

---
