# SPRINT 03

__Initial pull requests due Wednesday, October 18, end of class__. PR's will be addressed in the order received.

## Working Directory

Note the "dev" directory in the repository. This is where all of our work will be done.

We have started writing the code, so you have a framework to attach your features to. Note that there is no code in the "global" space; everything is in Javascript pseudo-classes. The latest ECMA standard supports object-oriented syntax (actual classes, as opposed to functions defined on functions), but it is not fully supported across all of our target devices/browsers.

Before you examine the code or run it, you may want the check out doc/buildGraphDemo.mp4 to see what it does.

One thing that might be confusing is where to use "this" and where to use "self." For certain class functions that are passed to D3 functions, for example, the class goes out of scope, and "this" refers to the D3 object, not the class on which the function is defined. To refer to the class on which such a function is defined, we pass the class object as a variable "self."

Our objective for now is to work only with d3.js and SVG; we will not be using any other Javascript libraries (not even jQuery), and we will do our best to avoid CSS.

D3 links:

* [https://d3js.org](https://d3js.org)
* [https://github.com/d3/d3/wiki](https://github.com/d3/d3/wiki)
* [https://github.com/d3/d3-selection-multi](https://github.com/d3/d3-selection-multi)

## Testing

Before pushing code and requesting a merge to develop, verify that your code works on the __LATEST VERSIONS__ of the following:

### Windows desktop

* Chrome
* Firefox
* Edge

### Mac Desktop

* Chrome
* Firefox
* Safari

### iPhone/iPad

* Safari

### Android

* Chrome
* Firefox

You may need to work together, checking out each other's branches, to cover all of these device/browser combinations.
 
## Sprint Assignments (initial PRs due beginning of class Wednesday, October 18):

__FOR ALL ASSIGNMENTS: with each new feature or modification, a new blackbox test should be added, if necessary, to test/blackbox.md__
__EACH TIME YOU PUSH CHANGES TO AN OPEN PULL REQUEST PLEASE ADD "@ajwnycct & @CarlosXViera: please check."__

### Cheng Chin
1. Create specification for and re-implement an "SVG scrollbox" for overlays. 
2. Add a one-pixel-wide white border around overlays.
3. Make sure the button provided by Brian does not scroll when text does scroll.
Coordinate with Brian; you both may submit a single PR for your joint work.

### John Cruz-Makuku
1. Link to the Santander Website when Santander logo is clicked.
2. Fix the issue where clicking an already pressed vertex in 'PLAY' causes a stash. You should be able to 'press' the vertex once but any following press should not add to the undo stack.
3. Change `graph` to `self` when calling `stash` in `graph`.

### Fanzhong Zeng
1. Investigate space after single quote in character:path hash; has the comma character issue been resolved?
2. Rebase local storage branch and create blackbox test.
3. Create a path->text "freeze" function, that outputs path or path(s) (potentially in a hash) so we can use without running append\_text. We must use append\_text dynamically for some tasks, such as matrix contruction, but other paths, such as help and about, should not use CPU cycles to paint text.
4. Investigate strategies for predicting when a press will result in an unwinnable game.

### Jermaine (Jia Ming) Feng
1. Look at optimizing graph.adjacency\_matrix() for a large number of vertices and edges.

### Brian Kriczky
Add a button at the top left corner of the matrix overlay to copy to clipboard. Coordinate with Cheng to move matrix data down and out of the way of the button. You both may submit a single PR for your joint work.

### Daniel Lux
1. Make the buttons on the the control panel unformly spaced.
2. Find out where buttons are rendered, and encapsulate in a function that takes width, height, spacing. x-position, and text scale arguments.
3. Vertically center the red line that closes the controls "door."

### Ian Pokorny
1. Add a SEQUENCE button and corresponding overlay. We want to display the value of graph.pressing\_sequence in an overlay, in the same way we do with matrix. Coordinate with Cheng and Brian.
2. When complete, open a new PR for fixing the Vertex leap-on-drag issue.

### TO DO IN FUTURE SPRINTS
Future features/bugs to address, in order of priority:
PHASE 1 - complete frontend  
1. Move analysis: predict when a move has rendered winning impossible.
2. General code optimization and naming conventions -- when to use camel case and when to use underscores?
PHASE 2 - begin backend
1. Store graph and associated pressing sequence in database.  
2. Recall a graph and associated pressing sequence.  
3. Playback a recalled sequence.  

