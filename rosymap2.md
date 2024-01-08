should have a link at the start of the readme saying something like 
'how to install R/RStudio'.

could link directly to 
https://www.youtube.com/watch?v=A-iwYU3X6_M&ab_channel=TheCodingDocs
Although, making essentialy a pseudo transcription of that video, 
with still images from it, would be helpfull, 
and would be able to be included in the paper.

very high level instructions 
(also me recording what I am doing.
for those who care, 
I am doing all of this in a windows sandbox,
so I can test from a 'clean' state)

these instructions are mostly the same as last time
if you skip down to the last secttion, you can see
the main new feedback

goto https://cran.r-project.org/index.html

where it says 'Download and Install R' clink the link associated
with your operating system.

for windows, this takes me to a page with a link that says
'install r for the first time, which I click on.

there is a link at the top of the page that says
'download R-<current version> for windows'.
note that '<current version>' may be different depending
on when you access the site, but at time of writing, for me it was
Download R-4.3.2 for Windows. Click on it.

this downloads an instalation exe. 
Navigate to your browsers downloads folder,
and run that exedcutable. Most common browsers should show
a little notification when you start downloading the file,
so there will probably be a helpfull pop up you can click
to run the executable.

select setup language : hit ok (it deafults to english)

gnu general public license : read the document, 
scroll to the botton, and press 'next'

select destination location: just hit 'next', 
to use the default instalation dir

select components : just hit next, 
accepting the default configuration

start up option : press next to accept defaults

select start menu folder : press next to accept default

select additional tasks : press next to accept defaults

it will then begin the instalation

press finish!

--------

now we need r-studio

go to https://posit.co/products/open-source/rstudio/, 
and click on the button that says 'download rstudio'

this will open a new page, with a 2nd 'download rstudio'
button, which we must press (confusing)

on the next page, scroll down and there are two buttons
'download and install r'
and
'download rstudio desktop for windows'
we already installed R, so let click on 
'download rstudio desktop for windows'

A new download starts. wait for it to finish, 
then run the executable

accept all defaults and install

-------

now, we want to open rstudio.
if you press the 'windows key', 
it should bring up the windows start menu.
if you start typing there, it will search files/etc.
type 'rstudio', and you should see the rstuio app 
show up in the search results. Run the app.

a 'choose r instalation' prompt comes up.
'use your machines default 64-bit version of r'
should be preselected, so just press ok.

rstudio will open. a prompt about automated crash reports
shows up, which you can say yes or no to. I said no.

on the left side of the rstudio screen, there is the 'console'
we will now enter text here. there should be a blinkcing text cursor
already in the window. you can click in that window and start typing
(are copy/paste text into it). if you hit the 'enter' key, 
the rstudio console wil try and 'run' what you have written currently.

paste the following into the console and press enter

install.packages("remotes") 
remotes::install_github("brandonerose/rosymap")
library("rosymap")

this will install/setup rosymap

now, we need to copy the example files to a location of our choosing.
using your documents folder, or desktop would mostly likely be fine.

in the windows sandbow I am using, the path to my documents folder is
"C:/Users/WDAGUtilityAccount/Documents", so I will use that.
you will need to pick your own folder.

so, I enter the following

set_dir(file.path("C:/Users/WDAGUtilityAccount/Documents"),F)

the offical rosymap page talks about tidygeocoder now.
I will skip that. For simplicity, 
I will leave out the conversion of addresses to lat/longs.
later on, I will just edit the example
excel files to demostrate that it is possible to get custom data
into rosymap

to launch rosymap, I do

run_app()

and then rosy map opens with the example data.

-----------------------

the last thing I will do, is upload some edited excel files.
click on the 'upload' icon on the left side of the rosy map app.
browse and find an events of interest and (optionaly) interventions
excel documents. in my case, I copied the example files and edited them.

well... I would have done that, 
but the app froze up again when I tried to upload a .xlsx file...
however, if I converted them to csv (comma separated values) files,
it was able to load them. so, that is a bit of a hitch, 
but I was at least able to get custom data into the app.

also, there does not seem to be any feedback when you press the 
'save your above files!' button. But, I presume if I close and re-open
the app, my new data will still be what is displayed?

