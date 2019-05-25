# 100 Days Of Code - Log

## Day 1: 18 May 2019

**Today's Progress**: Worked on a basic setup of TDD on React.

**Thoughts**: I have been making some React apps; all of them are using the
awesome create-react-app. I also have made a WordPress Gutenberg block, which is
React based, using create-guten-block. They are very great bootstrapping tools
to get a project going. But I've been wondering about the gears ticking behind
the scenes.

I found a great series about TDD on React that start from the basics of
toolings. Too bad it didn't use Webpack as I'm starting to get familiar with it.
But on second thought maybe we don't need it yet, just some basic stuff to do
testing on React.

Got some hiccups when I setup [Cypress](http://cypress.io). I've been doing the
challenge in my Windows machine and used WSL (Windows Subsystem for Linux). It
seems Cypress can't work with WSL, so I need to install it on the Windows side
rather. I don't know; maybe I'll continue on my Mac next time. It took quite
some time to get the setup working, but I think the basic setup to do TDD is
ready.

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)

## Day 2: 19 May 2019

**Today's Progress**: Complete a feature following basic TDD.

**Thoughts**: After completing the setup yesterday, I started working on the TDD
basic. I used Cypress for the End-to-End testing then made a unit test on the
internal functionality using Enzyme and jest. I still not clear on the testing
concepts on the things I've read. There are snapshot testing, unit testing,
behaviour testing, etc.

For unit testing, I think I already got the gist of it. Unit testing do the test
on the basic functions, for example, when we save data, we will use saveData(),
unit testing tests the saveData() to make sure it does what it was intended.

Another concept which I think I start to get the hang of it is the End-to-End
testing. The testing test what the users are expected to experience. So, on the
front-end react if there is an End-to-End button test will test the button
according to how the users will interact with it.

For these TDD basics, I'm following a series in
[CodingItWrong youtube channel](https://youtu.be/0aAdglT39go) supplemented with
some articles and the official documentation. I intend to work my basics here,
then rework some of my simple side projects in the past in TDD way (maybe my
react-kalkulator project).

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)

## Day 3: 20 May 2019

**Today's Progress**: Add styling using React UI Framework

**Thoughts**: I want to add some styling on the application. I've been working
with Bootstrap and want to try something else for this project.

I found out about
[Fabric UI from Microsoft](https://github.com/OfficeDev/office-ui-fabric-react).
It has React UI framework ready to use. I tried using it, but it seems like it
can't work nicely with Parceljs that I'm using here. Maybe if we use it in a
bundle with a build tool like Webpack, it can work better.

Regardless, I don't want to increase the complexity of this project. My goal is
to work on the TDD basics. So I looked for other UI Frameworks and found
[Grommet](https://v2.grommet.io/). It seems nice and have some themes packaged
with it.

I chose to use Grommet and managed to switch the basic UIs to it. I also managed
to add a feature to toggle light/dark theme with Grommet. Of course, in TDD way,
wrote the Cypress tests first then implement the feature.

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)

![Day 3 Progress](https://github.com/indralukmana/100-days-of-code/raw/master/screenshots/D3.gif)

## Day 4: 21 May 2019

**Today's Progress**: For today's progress, I tried CircleCI for Continuous
Integration. In the past, I have worked with teams that use CI in their
repositories. So when I made a pull request, there will be a CI checking whether
my PR was breaking anything. Honestly, I didn't know what it was all about. So
today I tried my hands on this.

I am not a DevOps specialist, so there are a lot of things I am not familiar
with in this process. I don't think we need to master everything in web
development. But I believe there is value to at least know about the gears that
support our development. CI I think is one of those things, because it will make
our flow in TDD automated when we work in a team.

I managed to connect my React TDD Practice with CircleCI. I got a lot of hiccups
when configuring Cypress with the CI. After fiddling with the configurations, I
managed to work the end-to-end test Cypress, unit test Jest/Enzyme, and linting
work with CI.

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)

![Day 4 Progress](https://github.com/indralukmana/100-days-of-code/raw/master/screenshots/D4.png)

## Day 5: 22 May 2019

**Today's Progress**: Playing around with Grommet Box layout and layer/modal.
Managed to put my form into the modal, centre the box for the general layout and
a new field into the form.

Before adding the new field, I add some unit test to drive the development.
After I added the field, my end-to-end test regressed. I then changed the test
to better suit the new field.

I was going to add form validation for the fields. But I'm still unsure where to
put validation in testing. Should I put it in the unit test (Jest/Enzyme) or
end-to-end (Cypress)? I think this should be in the unit test because I believe
there would be quite a lot of validation testing and end-to-end seems 'too
expensive' to test these.

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)

![Day 5 Progress](https://github.com/indralukmana/100-days-of-code/raw/master/screenshots/D5.gif)

## Day 6: 23 May 2019

**Today's Progress**: I managed to change the regular form to Formik today. Also
playing around the general Box layout of Grommet.

The validation also works nicely here. The form won't submit when the required
fields are empty or in wrong format. So it generally work.

I didn't do much on the testing part. But at least my previous tests are not
breaking.

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)

## Day 7: 24 May 2019

**Today's Progress**: So I was trying to implement the tests on Formik here. And
it is quite challanging. After reading through the docs and GitHub issues
regarding testing using Jest/Enzyme it is caused by the way Formik handle its
form.

So Formik is async and Jest is sync in nature. We need to do async-await or make
some promises if we want to do the test. I'm still not familiar enough with
Formik and Jest to do this. The examples I got seems quite complex and too
involved for my small TDD practice project.

So I'm taking a step back and re-evaluating my goals here. I want to get to know
the tools used in TDD and then try to implement it in this practice project. I
got to know end-to-end testing (acceptance test) with Cypress. I also get to
know how to use Jest/Enzyme to do unit test.

I think I managed to achieve my goal here for the first week. Next I want to
make a small project following TDD not too complex but also have enough depth
for me to play around with.

**Link to work:**
[React TDD Practice](https://github.com/indralukmana/React-TDD-Practice)
