# Codr 6×6 Onboarding Flow (Portfolio Excerpt)

This is the guided intake that prevents context sprawl and keeps agent builds spec-led (not brain-dump-led).


1 – What specific job or project do you want this agent to perform?
It’s best if you describe the main goal or outcome first.

Examples include a morning report of what’s due on your calendar and task list, a summary of emails in your inbox, or generating a specific KPI report.

> _have user click 'next' with arrow right icon to proceed to next question_

---

2 – What actions will this agent need to take to get that outcome?
Tell me the steps you take, in the proper order, when you complete this process yourself.

This is what I’ll need in order to create the proper LLM coded logic and API connection points necessary to automate your workflow process properly.

> _have user click 'next' with arrow right icon to proceed to next question_

---

3 – How do you want to engage with and ship intel to your agent?

Start with the easiest way to offload information in its current format that feels natural so it feels quick and painless to get it off your list.

**Preferred Platform**  [CTA style box for each item, changes color when selected]
Choose one.
~ Short web form
~ Chat interface
~ Button click
~ SMS or voice call
~ DM app or social platform
~ Email or internal comms model

> _have user click 'next' with arrow right icon to proceed to next question, using the same CTA style boxes for each item as the last category_

**Intel Input Format**
Click to select up to 3 formats. Click again to deselect if you change your mind

~ Voice to text
~ Text only
~ Live voice
~ File uploads or Public links
~~ MP3 or MP4
~~ PNG or JPEG
~~ PDF or TXT
~~ CSV or DOC file link with viewing permissions

> _have user click 'next' with arrow right icon to proceed to next question_

---

4 – Will this agent need to store or search data in real time?

> _have the user click a CTA style button to select 'Yes' or 'No' with state color change, then have user click 'next' with arrow right icon to proceed to next question. If user chooses yes, proceed with the following asks for them to share their parameters, one at a time into a short text field in the chat thread. Have user click 'next' with arrow right icon to proceed to each parameter question until complete_

Share those database parameters for me now.

~ what type of data
~ where’s it coming from
~ how you’d like to filter or sort it
~ how long should it stay catalogued
~ where to archive it
~ will you need status updates

---

5 – What will trigger this agent to run? [CTA style box for each item, color change on select]

~ automatic based on a scheduled date
~ an action in your app interface
~ a message in your preferred comms channel

> _have user click 'next' with arrow right icon to proceed to next question_

---

6 – Is there a next project or process you want to trigger once this agent completes its JTBD after you're done testing this prototype?

This is how I’ll be sure to keep the code agile for new connections and automations after this prototype is tested and proven consistent.

> _have the user click a CTA style button to select 'Yes' or 'No' with state color change, then have user click 'next' with arrow right icon to proceed. If user chooses yes, reveal a short text field in the chat thread with the label 'Workflow to trigger for future app upgrades' Have user click 'next' with arrow right icon to proceed to style questions_

STYLE QUESTIONS FOR NDs

Let's give your app some flair.
1 - Theme - do you prefer
A - Light | B - Dark | C - Either works for me

2 - Color Palette - do you prefer
A - Monochromatic with on-brand color pops | B - Bright | C - Muted | D - Neutrals | E - Black & White

3 - Font - do you prefer
A - Geometric | B - Book style typeface | C - Code style typeface | D - Display with san serif combo

4 - Design vibe - do you prefer
A - Simple and minimalist | B - Clean and Maximalist | C - Corporate | D - Boho and Feminine | E - Playful and Engaging

5 - Motion effects - do you prefer
A - None | B - Elements only | C - Text and Elements | D - Page or Scroll transitions | E - Surprise Me

6 - App you love - optional
If you could name one SaaS tool, web app, or iPhone app you love using because it's design makes the task you're working on feel easier, energizes you, or lightens your mood, what app would that be? Answer with the name and drop a link to it, if you've got one.

Otherwise, click 'skip it' (CTA box in chat thread)

7 - Screenshots to share - optional
Upload up to 3 image files or screenshots below that show design elements you're inspired by and want to mirror.

Categories worth a share include: 1 - design vibe | 2 - icons, shapes, imagery | 3 - color palettes and fonts

Otherwise, click 'skip it' (CTA box in chat thread)

[The vibe coder agent should then compile a summary of the user's replies as a short bulleted list that looks something like what I add below and asks, Everything look good? Click 'code it' (a CTA box in the thread) if yes or 'fix it' (a CTA box in the thread) for quick changes

[If user selects quick changes, prompt them to answer if they want to A - start app flair quiz over | B - change a specific question number, then show them the options again for that questions so they can choose it.

When they're done, ask if there are any other edits with this same style in chat prompt thread with box choice All set? Click 'code it' (a CTA box in the thread) if yes or 'edit another' (a CTA box in the thread) and ask for the number of the question, proceed as before showing question and options and confirmation messages until user gets to code it and submits the app to be coded and previewed]
