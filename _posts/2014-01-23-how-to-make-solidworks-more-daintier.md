---
layout: post
title:  "How to Make Solidworks More Daniter"
date:   2014-01-23 20:03:05 -0800
categories: solidworks 1337 hax
---
Today at work I was struck by how dainty the SolidWorks rollback cursor was.

It looks a bit like this:

![roll back tool](/images/solidworks/rollback.png)

"Sure, that's dainty. BUT IS IT DAINTY ENOUGH? CAN WE MAKE IT DAINITIER?"

I thought, "Sure, that's dainty. BUT IS IT DAINTY ENOUGH? CAN WE MAKE IT DAINITIER?"

Or you know, exactly like that. I thought, "Sure, that's dainty. BUT IS IT DAINTY ENOUGH? CAN WE MAKE IT DAINITIER?"

![dainty as fuck](/images/solidworks/pinky-up.png)

The answer is yes, but it took a bit of hackery to do so.

I used a program called [IconsExtract](http://www.nirsoft.net/utils/iconsext.html) (thanks Mike!) to search all the .dll's in Program `Files\SolidWorks Corp\SoldWorks\` and accompanying sub-folders. I found two instances of the rollback cursor:

`SolidWorks\lang\sldres1u.dll`
`SolidWorks\sldassybomu.dll`

The one you want is `sldres1u.dll`. I'm not sure what a bomu is. Maybe something in one of the BOM tools? Also, this might be different if you're using something other than SolidWorks 2014.

If you're following along at home, note down the locator number thingy, it'll come in handy later. This little guy is 1404.

Once I had created the Pinky Up version of the rollback cursor in [Icofx](http://icofx.ro/) (my first time using it, or ever doing icon/pixel art, seems legit), I used [Resource Hacker](http://www.angusj.com/resourcehacker/) to edit the sldres1u.dll. If you'd like to try this, for fuck's sake, back up that DLL before you go "hacking" it. Once I had the DLL open, I opened the Cursor Group, located cursor 1404 and replaced it with my custom  one. You'll probably have to save your modified DLL somewhere other than directly into the `SolidWorks\lang` folder due to permissions, but assuming you've got administrator privileges you can copy it in there later.

![final result](/images/solidworks/final-result.png)

Because I had to shift the hand down a bit to fit the pinky in there, it doesn't map the same way it used to, but you'll adjust.

If you'd like to borrow my icon, it's [here](/images/solidworks/dainty.cur). Dassault, please don't sue me.

*UPDATE 2014-01-24*: [As @mivanov pointed out](https://twitter.com/mivanov/status/426755134039683072), you can totally [use Visual Studio to change the hotspot of a cursor](http://msdn.microsoft.com/en-us/library/0b1674x8.aspx). Actually, you could probably use Visual Studio to do everything I've outlined here short of searching all the cursors.