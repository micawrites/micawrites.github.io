I recently read Carnie (2010)’s _Constituent Structure_, a fantastic post-intro syntax textbook about syntactic structure. 

Chapter 2 lays out some clear, succient evidence for motivating hierarchical structure in syntax. There are two (very different) pieces of evidence from that chapter that I think are pretty accessible to someone who’s never learned syntax before and I thought I would recapitulate them here.

I don’t really modify Carnie on the first piece of evidence, but I tried to reframe the second piece of evidence in a clearer manner.

## Constituency tests

This first piece of evidence is, I think, the strongest and most basic. There are syntactic processes that favor certain strings of words over others.

These are called constituency tests. Here are some examples.

- Pronoun replacement: [The king of England] is dead → [He] is dead.
- Passivization: We made [some mistakes] → [Some mistakes] were made.
- Fronting: We will [win the fight] → [Win the fight], we will.
- Deletion: I am [going to the store] and they are also [  ].
- One-replacement: I wanted the big [book about linguistics], not the small [one].
- Do-so-replacement: I [walked in the park] and they [did so] on the beach.

The fact that these strings are favored suggest that they act like a unit. Constituency tests can also target units embedded within other units, suggesting that syntax has a hierarchical (grouped) structure.

- I wanted the big [red book about linguistics], not the small [one].
- I wanted the big [red book] about linguistics, not the small [one] about history.

## Insufficiency of precedence

The second piece of evidence is more mathematical. It says that precedence alone is not enough to capture all syntactic structures. Assume syntactic structures are based on precedence. For example, the sentence “They said that the party was bad” could be represented like the following.

![](/assets/images/they%20said%20that%20string.pdf)
	
Syntactic structures also show repetition. You can say “They said that they said that they said that the party was bad”. We can represent this using loops.

![](/assets/images/they%20said%20that%20loop.pdf)
	
To get technical, this notion of precedence has the properties of being reflexive (A → A) and transitive (A → B → C implies A → C). However, some syntactic patterns are not expressible by reflexive-transitive precedence. My new favorite example, which Carnie republished from Lasnik (2000), who said he got it from Morris Halle, is originally I think from a [Rocky and Bullwinkle clip](https://www.youtube.com/watch?v=-JVlUHxf8iY&feature=youtu.be&t=21).

> Well last time Bullwinkle had tossed Rocky high into the air in a desperate attempt to intercept the misguided **missile** which was carrying, of all people,  Fearless Leader himself. But the evil-minded villian thought Rocky was an American **anti-missile-missile** and so began to assemble his secret weapon, an **anti-anti-missile-missile-missile**.

The pattern strings together `n` *anti* ’s followed by `n+1` *missile*’s. However, we cannot describe this pattern by looping over words, since precedence doesn’t let us count how many times we pass through a loop. That is, reflexive-transitive precedence is insufficient.

![](/assets/images/anti%20missile%20loop.pdf)

Instead, we need a richer structure, like trees, which we can stack on top of each other.

![](/assets/images/anti%20missile%20tree.pdf)

## Summary

To recap, the evidence for hierarchy in syntax is that (1) there are tests that single out constituent strings of words within other constituent strings and (2) precedence can’t capture the range of possible syntactic patterns. There’s more complicated theory-internal evidence that Carnie brings up---binding theory and c-command, subject-auxiliary inversion---but it requires more setup. The two pieces of evidence above are accessible to a non-linguist without having to list too many examples.

## References

Carnie, A. (2010). Constituent structure (Vol. 5). Oxford University Press.

Lasnik, H., Depiante, M. A., & Stepanov, A. (2000). Syntactic structures revisited: Contemporary lectures on classic transformational theory (Vol. 33). MIT Press.