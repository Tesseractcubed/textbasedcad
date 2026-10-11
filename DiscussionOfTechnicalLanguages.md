
One of the many (obvious) nuances of using text to hold CAD data... is that text is text, and CAD data isn't.

How do we overcome this issue?

Well, we have to do several things:
*Define a text standard
*Define operational words, what they mean, and how programs and the user should interpret them
*Define how a program sould interpret words when they don't have the native feature another software used
*Define directions, naming conventions, and other details

One of the big things we'll have to set up are what features we'll support. As I'm (Jacob) am the only developer on this project, I would like to propose several less intuitive things, and several more intuitive things should run together.

For the less intuitive things...

First let us create multiple ways of designating the same specific (meaning after just one step) outcome. Similar to natural language, technical language inherits abbreviations, prior process steps, and overall a less rigid set of grammar and lexicon. Also, different programs call different things the same word, and the same things different words.
Second, let us typically use certain common frameworks, and also allow the user to completely diverge from them given the user provides the specificity to enable repeating their path. But this sounds like an idea with lots to go wrong... why? Well, we can't predict how users want to use the software; enabling 
Third, the goal of supporting T splines, B splines, G3 curvature, boolean operations, and, if we're insane and code correctly, higher dimensional modelling (this last one is a reach goal, if ever there was one). Why support these complex surface modelling tools? 
Fourth, built in support for meshes, both surface meshes and three dimensional mesh grids.

More intuitive, or at least understandable, design choices:

*Patterned elements are treated as fully editable, both the element to be pattered and the pattern details
*Zero thickness geometry is not addressed in this software tool at the moment
*Absolute, Local, and Relative dimensions are all allowed in the same sequence (just like G-code). This is mainly to allow users to create elements that are fixed to a specified point. The names need work though, like all of these overlapping coordinate system reference location schemas do.
*Dimensions and Relations can be relative to existing components, or some arbitrary location / angle reference in the default space or user defined space definitions. This enables things like dimensions from vertical, from a default axis / plane, etc.
*2D sketches and 3D sketches are both supported, but with a heavy preference for 2D sketches.
*Inheritance is relatively loosely defined in this standard, but is probably the most important tools to specify. As I see it, inheritance into new 2D geometry is composed of projecting 3D geometry onto the work plane, or examining the intersection of the 2D work plane and the existing 3D geometry.

... Not sure what to write now. This project seems to get thrice as big as the words I write.