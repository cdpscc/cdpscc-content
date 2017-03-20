+++
date = "2017-03-18T14:36:58+13:00"
title = "Parallel Scratch"
tags = ["scratch"]
categories = ["scratch"]

+++

*Note: this is still just a draft...*

In some of your Scratch projects so far, you might have seen some scripts that look like this:

```blocks
forever
  if <key [up arrow v] pressed> then
    change y by (10)
  end
  if <key [down arrow v] pressed> then
    change y by (-10)
  end
  if <key [left arrow v] pressed> then
    change x by (-10)
  end
  if <key [right arrow v] pressed> then
    change x by (10)
  end
end
```

This code follows a single line of steps one after the other. This approach has only one step running at once. Scratch can only ever be reacting to one key at a time.

What would it look like if we split that up so that Scratch did more of the work behind the scenes, and our code did less work?

For example:

```blocks

when [up arrow v] key pressed
change y by (10)

when [down arrow v] key pressed
change y by (-10)

when [left arrow v] key pressed
change x by (-10)

when [right arrow v] key pressed
change x by (10)

```

Now we have five less blocks, the code is smaller and hopefully faster. Not only that, Scratch can now react to multiple keys at a time internally. We now have multiple code blocks running in _'parallel'_.

We can make our projects more flexible by reacting to different Scratch events like this rather than creating one big loop with lots and lots of **if** checks in them.
