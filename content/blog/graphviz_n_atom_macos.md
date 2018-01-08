## DOT-diagrams series: GraphViz in Atom.io on macOS.

Note. Everything in this guide will apply to macOS (10.13.x High Sierra), unless otherwise stated. Also, where it is possible this article will refer to third patty guides to minimise the size of this guide and do not re-invent a bicycle.

I was recently advised by our CISO to start visualising processes and tasks by utilising DOT-language. I had never used it. After spending few hours in research on this subject, I realised, that there were few ways to skin a cat, as always. Meantime, I have been using Atom for editing different scripts and, again, our CISO showed how he utilised Atom to build quick DOT-graphs. So, I decided to stop my attention at this solution.
As a result, the main reason for writing of this blog post was a lack of a straight forward guide on configuration and usage of GraphViz in Atom. 

This guide will introduce one of the ways building graphs with text (DOT-language style) and text editor such as Atom. There are different ways of creating graphs with DOT-language. 
To name few:
- In online editor, eg: [WebGraphViz](http://www.webgraphviz.com/)
- IDE/text editor + GraphViz application [+ IDE Plugins]
- RStudio + R + DiagrammeR

The first option in the above list is the fastest way to start building your graphs with DOT-language. You just simply need to run that website in your favourite Internet browser, eg Mozilla Firefox, Google Chrome, Internet Explorer or Safari. And start building DOT-diagrams. So, I believe, this option does not require much attention. 

Today, I will stop my attention at the option 2: “IDE/text editor + GraphViz application [ + Plugins]”. The latter means, that in order to build DOT-graphs we will need to utilise the following 3 main tools:
1.	GraphViz application – to be able to convert DOT-text into grpahs.
2.	IDE/Text editor – which is Atom.io for the purpose of this article.
3.	Atom GraphViz plugin(s) – visualise Dot-diagrams in real-time within Atom.

### Install GraphViz application
#### Install Homebrew
In order to install GraphViz application, firstly, we will need to install Homebrew (package management software). In Terminal type the following command (all in one line):
<br>` /usr/bin/ruby -e "$(curl –fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" ` </br>
Then hit Enter/Return key.
In Terminal, you will see the list of actions the above CURL command will proceed and it will ask you to either confirm or cancel the installation with this line:
<br>  `Press RETURN to continue or any other key to abort`  </br>
Hit Return key on your keyboard. 
At this stage, it will ask you to provide your login password. Type your password in Terminal, after the word ‘Password:’.
Once Homebrew is installed you will see confirmation as it’s shown on the below screenshot followed by your machine and user names ending with $ :

![]/(img/blog//gv1_image1.png)

To confirm that brew was successfully installed run the below command in Terminal:
<br>  `  which brew ` </br>
If you see `/usr/local/bin/brew` then Homebrew was installed successfully.

#### Install GraphViz
Now, in Terminal type the following command:
<br>  `brew install graphviz` </br>
Then hit Enter/Return key.
GraphViz modules will begin their installation. Once the latter is complete, you will see again your machine and user names ending with $.

To confirm that GraphViz was successfully installed run the below command in Terminal:
<br>  `which dot` </br>
If you see `/usr/local/bin/dot`, then GraphViz was installed successfully.

Other options for GraphViz installation can be found [here](http://www.graphviz.org/download/).

### Install Atom.io
In order to install Atom text editor on your Mac please follow [this guide](http://flight-manual.atom.io/getting-started/sections/installing-atom/#installing-atom-on-mac).

Once, you installed Atom, make sure that you run “Install Shell Commands” from within Atom by either following the steps in the above article or by clicking the relevant menu option in Atom’s top menu bar. See screenshot below:

"/img/blog/gv1_image2.png"

### Install GraphViz Plugin(s) on Atom
I am sure there are few Atom plugins for GraphViz real-time visualisation and preview out there, however, I found the below two the most convenient for my tasks, so far.
- Markdown Preview Enhanced plugin
- Graphviz Preview Plus plugin

#### Install Markdown Preview Enhanced plugin
In Atom go to Atom menu -> Preferences -> +Install
In the search field under + Install Packages type the name of the plugin to be installed, which is markdown-preview-enhanced. Then click *Packages* button -> click *Disable* button next to markdown-preview -> click *Install* next to markdown-preview-enhanced plugin. See screenshot below.
 
"/img/blog/gv1_image3.png"

The Markdown Preview Enhanced plugin will be installed once the above steps are complete.
 
Other installation options of Markdown Preview Enhanced plugin can be found [here](https://shd101wyy.github.io/markdown-preview-enhanced/#/installation).

Use case of Markdown Preview Enhanced plugin with DOT-language.

"/img/blog/gv1_image4.png"

Before you can preview files with DOT-diagram you will need to save your DOT-text file with either `.md` file extension. 
To initiate preview of the graph hit combination of the following keyboard keys `ctrl+shift+m`, while in Atom,  once file is saved.
See more examples [here](https://shd101wyy.github.io/markdown-preview-enhanced/#/diagrams?id=graphviz). 

#### Install GraphViz Preview Plus plugin (optional)
Alternatively, you can install another Atom’s plugin [graphviz-preview-plus] for pretty much the same purpose of real-time preview of the DOT-graphs. 

"/img/blog/gv1_image5.png"

You may receive the below message to install language-dot dependency for the plugin. Click *Yes*.

"/img/blog/gv1_image6.png"

Now, you can use this plugin to visualise graphs from DOT-language on your Mac in real time.
Before you can preview files with DOT-diagram you will need to save your DOT-text file with either `.dot` or `.gv` file extensions. 
To initiate preview of the graph hit combination of the following keyboard keys `ctrl+shift+v` once file is saved.

"/img/blog/gv1_image7.png"
 
See an example [here](https://github.com/sverweij/atom-graphviz-preview-plus/blob/master/README.md).
