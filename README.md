# Introduction

Open CAD Components Interface (OCCI) is a way to distribute platform-independent parametric CAD (Computer Aided Design) content on the web. It is powered by open source Script CAD engines like CadQuery (and possibly endless others) that can define parametric CAD models with code instead of clicking. 

# Why OCCI: open source parametric design for all, everywhere

There is a lot of CAD content available online on public platforms (like GrabCAD, 3D Content Central) or within software ecosystems like Autodesk and OnShape. 
Most of these models are static and closed source. Which means you can not parametrically change them as an user or view and modify the source of the model as an author. 
This is because they are designed by drawing in (mostly proprietary software) and then saved as a model in a format which either belongs to that software or a general open format like STEP or STL. In this way most publically available CAD models lose the valuable possibility to be customized. They also hide the logic of their design and show only the outcome. 

Script CAD - like OpenSCAD and CadQuery - can offer an alternative by defining the model with a scripting language that can be easily changed by pre-defined parameters or viewed and altered just as any piece of software. In addition to that, these CAD script engines are open source: which means that your CAD script is fully portable to be run everywhere, for free and that will remain so. 

Script CAD has been steadily growing and there is already a lot of content available. But most of it is fragmented and not really online. This is where OCCI comes in. It aims to offer open source, platform-independent parametric CAD content for all, everywhere. 

# So what is OCCI concretely?

Very plainly OCCI encompasses these elements:

1. [occi-cad-spec](https://github.com/occi-cad/occi-cad-spec) A set of specifications on data structures and REST API’s that enable CAD scripts to be executed parametrically and distributed on the web which we’ll document in this repository
2. [occi-server](https://github.com/occi-cad/occi-server) A reference stack in accordance with the specification that organizes a library of CAD scripts, caches and executes them on request of the user through a REST API. It is the fastest way to publish a CAD script as a web API.
3. [occi-freecad-plugin](https://github.com/occi-cad/occi-freecad-plugin) A proof of concept plugin for FreeCAD that can manage OCCI libraries, search and query them for parametric CAD content
4. [scriptlibrary](https://github.com/occi-cad/scriptlibrary) A growing library of CAD components that we will host on our upcoming official OCCI server

# Example using the OCCI API

We have a test OCCI server available. Just use these urls in your browser to get parametric CAD content:

* [https://occi.archiyou.nl/cqwarehouse/nut/](https://occi.archiyou.nl/cqwarehouse/nut/) - Get the default nut model in STEP format
* [https://occi.archiyou.nl/cqwarehouse/nut?SIZE=M1.6-0.35](https://occi.archiyou.nl/cqwarehouse/nut?SIZE=M1.6-0.35) - Get a M6-0.35 nut in STEP format
* [https://occi.archiyou.nl/cqwarehouse/nut?SIZE=M1.6-0.35&format=stl](https://occi.archiyou.nl/cqwarehouse/nut?SIZE=M1.6-0.35&format=stl) - Get a M6-0.35 nut in STL format

Other examples of OCCI API functionality:

* [https://occi.archiyou.nl/docs](https://occi.archiyou.nl/docs) - Get generated API docs swagger.json
* [https://occi.archiyou.nl/search?q={{SEARCH_STRING}}](https://occi.archiyou.nl/search?q=box) - Search the OCCI library with a text string and get all scripts
* [https://occi.archiyou.nl/search](https://occi.archiyou.nl/search?q=box) - Get all scripts in OCCI library
* [https://occi.archiyou.nl/cqwarehouse/nut/1.0/params](https://occi.archiyou.nl/cqwarehouse/nut/1.0/params) - Get params of version 1.0 of the nut script

# Example using with FreeCAD plugin

Video

# For whom and contributions

* CAD script author: You can publish your CAD content to the web. See [occi-server](https://github.com/occi-cad/occi-server) to get started. 
* CAD content user: To get a sense of how easy it is to get free parametric CAD content inside your favorite CAD software try out the [OCCI FreeCAD plugin](https://github.com/occi-cad/occi-freecad-plugin). 
* Library contributor: If you have great parametric script CAD content and want to contribute to our upcoming OCCI library of CAD content please contact us or create an issue in our scriptlibrary repository
* Plugin creator: Want to contribute by making an OCCI plugin for your favorite CAD/3D software (like Blender, SolidWorks, OnShape) check out this spec or contact us
* Online viewer developer: We like to create a light-weight webviewer on top of the OCCI API. Let us know if you share that interest!

# License

All our code is licensed under the permissive Apache2 license. All CAD content is licensed under the given license type in the library.

# Supported by the Open Toolchain Foundation

Development of OCCI has been partly funded by the [Open Toolchain Foundation](https://opentoolchain.org/). 

