##  Story

Story is a set of generators to produce Clay commit messages.  The actual messages are stored in a file in Clay, effectively using a Clay as a database.  The generators are instrumented through `%hood`/`%helm` so they can pass notes to Arvo.

```hoon
> |new-desk %tale

> |mount %tale

> |cp /===/mar/story/hoon /=tale=/mar/story/hoon
+ /~zod/tale/2/mar/story/hoon

> |cp /===/sur/story/hoon /=tale=/sur/story/hoon
+ /~zod/tale/3/lib/story/hoon

> |cp /===/lib/story/hoon /=tale=/lib/story/hoon
+ /~zod/tale/4/lib/story/hoon

> |story-init, =desk %tale
+ /~zod/tale/5/story

> +story-read, =desk %tale

> |story-write 'Short message' 'Long descriptive message', =desk %tale
: /~zod/tale/6/story

> +story-read, =desk %tale
commit: 0vn.l7i50.emt3e.79vbv.tjuv6.ftaqk.pos61.iqa5q.j0jq4.7mn92.vjssn
Short message

Long descriptive message
```

Story is supported in `%base`, but you'll need to make the mark available on the target desk as done here.

- Story was originally written by @ynx0, e.g. [urbit/urbit 78468dc](https://github.com/urbit/urbit/commit/78468dc8ee4804b71d2010db4733e4650b827722).
