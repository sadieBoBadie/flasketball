Activity: Flasketball Bug Hunt
==============================

The “Hook”
----------

If you have any personal anecdotes fixing bugs, share them. You may also have students share the most difficult bugs they've encountered so far and how they've resolved them. One of the objectives of this activity is to emphasize the inherent value in _the daily process_ of resolving issues.

The “Why”
---------

As a developer, you WILL be working with unfamiliar codebases that someone else wrote. Being able to navigate and fix small-ticket bugs in such codebases will likely be one of your first tasks as a junior developer.

### Guiding Questions

*   What are some strategies you've employed to debug an error or unexpected behavior?
    
    _**Also see Review Questions at the bottom of this module**_
    
### Notes & Resources

Student Instructions

[download](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660274049__Flasketball Student Instructions.docx) | [google doc](https://docs.google.com/document/d/1bMtnQ0UOudqo429GX0NNDpgYB0EUkKVJMV-cfvAJ5pk/edit) Please make COPY

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660243112__student_instructions_thumbnail.png)

Review Slides (Optional)

[download](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660274099__Flasketball Walk-through Slides.pptx) | [google doc](https://docs.google.com/presentation/d/1EMojckrp_yjO-mqaftin-QE8iRkThv_g3m4b2IhRTic/edit#slide=id.g1438a413c28_0_100) - Please make COPY

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660243127__error2_soln_img.png)

Debug Files ([download](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660277483__FlasketBallBroken.zip))

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660243162__dashboard.png)

### Forms of Participation

*   Alone - Write down or answer opening questions in chat or DM
*   Class discussion
*   Pairs or groups

Roles:

*   Note taker
*   Time keeper
*   Researcher
*   Group Rep
*   Driver (pairs)
*   Navigator (pairs)

Instructions
------------

1.  **Intro (<5 min):**
    *   **Discussion:** Discuss debugging. See "hook" and "the why" for topic suggestions.
    *   **Activity Set up:** Run the fixed version of the Flasketball code and show students the working features in your browser, walking through how the features should behave. Allow time for any questions.
    *   **Roles:** Be sure students understand that at least one person will need to take notes on the bug and how they solved it to post in discord (or wherever medium makes sense for your class).
    *   **Expectations:** Review the student directions hand-out with everyone
2.  **BREAKOUT GROUPS (~15-20 min):**
    1.  Students do not have to finish all the challenges, but you may want to go longer to let them finish if it's going well.
    2.  Rotate, check on and help groups.
3.  **Presentations (~10 min):**
    1.  Have groups present / share their docs.
    2.  **Review Options:**
        1.  Review errors with the slides
        2.  Go through the broken version of the code with the class' help or calling on an individual student to 'drive' (shared screen and typing) as the class navigates or navigate as you, the instructor 'drives'
4.  **Reflection:**
    
    *   Do you develop incrementally? If you build and test one feature at a time, or only debug one error at a time, it is much easier to localize a problem.
    *   How do you test your assumptions? Use print statements or a debugger!
    *   If you have a hunch, what are the assumptions you are making? For example, is the value of that variable what you think it is? Is it even running that function right now? How do you know? Assert or test your assumptions before changing any code.
    *   How do you find what code to look for? (Reading the entire error message, backtracking and stepping through the code from where the error occurred, using print statements to confirm where the execution got to at each step.
    
    References: [Cornell Debugging Techniques](https://www.cs.cornell.edu/courses/cs312/2006fa/lectures/lec26.html)
    
5.  **Self-Assessment:** What did you learn? (See 'How Will Students Know They Were Successful')

How Will Students Know They Were Successful?
--------------------------------------------

*   Come away with a written list of encountered errors and the solution used
*   Can articulate at least one strategy they found helpful and will use going forward

Quick Reference ~ Error Solutions
---------------------------------

### Error

### Solution

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660153231__error1_405.png)

Missing method attribute in html form:

<form action="/enter" >

Change:

<form action="/enter" method="post">

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660153727__error2.1_BadRequestKeyError.png)

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660153737__error2.2_BadRequestKeyError.png)

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660162380__error2_soln_img.png)

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660240638__error3_TypeError.png)

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660240638__error3_immutable.png)

Mistakenly tries to update values in `request.form`, intent is to save form input values in session.

request.form\['first'\] = session\['first'\]
request.form\['second'\] = session\['second'\]
request.form\['third'\] = session\['third'\]

Switch the dictionaries to the other side of the assignment operator.

session\['first'\] = request.form\['first'\]
session\['second'\] = request.form\['second'\]
session\['third'\] = request.form\['third'\]

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660241502__error4_400_badreq_keyerror.png)

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660241513__error4.2.png)

In this case, not a problem with the form name and key names in the server. Because neither form nor method were designated for POST request, `request.form` is empty and form data was sent through the url as query parameters.

`leaderboard.html`

<form action="/changeRanks" method="post">

`server.py`

@app.route("/changeRanks", methods=\["POST"\])

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660242555__error5.1_rank_error1.png)

![](https://s3.us-east-1.amazonaws.com/General_V88/boomyeah2015/codingdojo/curriculum/content/chapter/1660242577__error5.2_rank_soln.png)