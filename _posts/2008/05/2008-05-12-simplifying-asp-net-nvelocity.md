---
title: "Simplifying ASP.Net - NVelocity"
slug: simplifying-asp-net-nvelocity
date: 2008-05-12 15:53:08 -0500
category: 
external-url: http://simpable.com/code/nvelocity/
hash: 2caf72cbae3d4e2b8c0430ac83070c71
year: 2008
month: 05
scheme: http
host: simpable.com
path: /code/nvelocity/

---

NVelocity[1] is a .NET port of the Velocity open source template engine. I have used NVelocity quite a few times over the last couple of years.
  CSBTL - this project never went public, but basically it removed the need to understand web forums and complicated server controls for building Community Server blog themes.  Graffiti - Graffiti supports a very simple theming model which enables building new themes with no knowledge of web forms and/or ASP.Net While you have more options using aspx pages, I generally prefer the simplicity of doing web pages via NVelocity. There are no complicated server controls, complete control over the markup, simple extensibility, and no need to jump between contexts when iterating over a list. 
 With this in mind, I was very happy to find the NVelocityViewFactory as part of the MvcContrib project. With just a couple configuration steps, I was able to use NVelocity views for my ASP.Net MVC projects. Sweetness! 
 For example, Phil Haack, has a post which discusses options to doing a simple repeater. This could be greatly simplified with NVelocity (see below). No code needs to be written, no context switching for properties, etc.
  <table>#foreach($hobby in $hobbies)  <tr class="#if($velocityCount % 2 == 0)row #else alt-row #end">    <td>$hobby.Title</td>  </tr>#end</table>
In addition, using fancy loops we could easily add content to be shown if it is empty and better structure our markup.


#foreach($hobby in $hobbies)#beforeall    <table>#before    <tr class=#even    "row">#odd     "alt-row">#each    <td>$hobby.Title</td> #after    </tr>#afterall    </table>#nodata    <h3>Sorry, no hobbies</h3>#end
The above example takes it to the extreme (all parts are optional), but should give you an indication of power available to you, again, all without requiring you to write a single line of code.

[1] As mentioned on the Castle site, the original NVelocity project seems to be dead. I have been using the updated version of Castle and recommend you use this version as well.


Posted to Code 
 and tagged as 
nvelocity
,
open-source
,
mvc
,
castle
,
graffiti
,
cs



Similar Posts

Castle Project
Unfuddle == BaseCamp For Developers
What Software do I use on the Mac?




