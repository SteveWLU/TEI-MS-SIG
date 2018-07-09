# Issues on Chapter 11 of the TEI Guidelines

## technical information
Issues refer to https://github.com/TEIC/TEI/blob/dev/P5/Source/Guidelines/en/PH-PrimarySources.xml.
If an issue refers to single lines of this chapter, the link on these lines should include a commit which makes this reference permanent. 

## issues already submitted to TEIC

### notable open issues
* [Restructure chapter 11 (#1427)](https://github.com/TEIC/TEI/issues/1427) 
* [ Merge 11.3.1.6 and 11.3.4.4 (#1477)](https://github.com/TEIC/TEI/issues/1477)

### lists
* [all issues opened by created by brettttt](https://github.com/TEIC/TEI/issues?utf8=%E2%9C%93&q=is%3Aissue+author%3Abrettttt+)
* [all issues opened by gerritbruening](https://github.com/TEIC/TEI/issues?utf8=%E2%9C%93&q=is%3Aissue+author%3Agerritbruening+)

## new issues
according to the current structure of the chapter 

### adjust introductory paragraph to ch. 11
* section: 11
* see issue #5

#### (short description, justification)
As part of https://github.com/TEIC/TEI/issues/1427 it would make sense to adjust the introductory paragraph of chapter 11.
This includes a brief comment about document-focused and text-focused transcription.

#### (suggested wording)
This chapter defines a module intended for use in the representation of primary sources as facsimiles and transcription.
The TEI offers two basic approaches for the encoding of such materials, one that views the intellectual units of communication as the 
fundamental hierarchy and one that takes as its primary concern the physical arrangement of text on the inscribed surface. 
In the discussion that follows, these two approaches are, for the sake of convenience, sometimes termed "text-focused" and 
"document-focused." 
This usage is not meant to imply a rigorous theoretical distinction between "text" and "document," however. 
Nor does the emphasis in the current chapter on the second approach imply a preference for that approach. 
Those whose goals are better served by the latter approach are advised to use the guidelines from the current chapter in conjunction 
with those found in other chapters, especially _________

### `@ulx` etc. on `zone`
* section: 11.1
* see issue #6

### rotation center for `@rotate`
* section: ?
* see issue #4

Speaking of rotation without clearly specifying a rotation center is unapplicable. Here is what we have for the **rotate** attribute:

#### current version
> indicates the amount by which this zone has been rotated clockwise, with respect to the normal orientation of the parent surface element as implied by the dimensions given in the msDesc element or by the coordinates of the surface itself. The orientation is expressed in arc degrees.

The phrase "with respect to the normal orientation of the parent surface" is not specifying a rotation center (what doest it specify actually?). Does that mean, we rotate zones around the ulx/uly values of the parent surface?  How/Where is the "normal orientation of the parent surface" defined? How does a "normal orientation" translate into a rotation center (a point)? What if the parent surface is a non-rectangular polygon? 
Or do we by default rotate around the ulx/uly of the zone element itself (which is more reasonable)? What if the zone is a non-rect polygon? I assume in the latter case the best default rotation center would be the first point of the polygon (that is: of the **points** attribute value)?

We should then add some prose to the Guidelines to define the default rotation center. Something like: 

#### revision draft

> By default the rotation center is given by the upper left corner of the zone (`@ulx`/`@uly` attributes). If the `zone`is a non-rectangular polygon, the default rotation center is given by the first point of the polygon (`@points`attribute).

Additionally, we should provide a way to define the rotation center manually (e.g. an additional attribute). It is unclear, if the proposed solution for default values is the best. Important is, that we define default values at all.

### change datatype of `@rotate` to `teidata.numeric`
* section: ?
* see issue #3

### Reconsider heading "Marking up the Writing Process" 
* section: 11.3.4

It is not clear
* why other sections (11.3.1 Altered, Corrected, and Erroneous Texts; 11.3.1.6 Cancellation of Deletions and Other Markings) should have nothing to do with the writing process
* why substitutions are categorically distinct from transpositions

The historic reason for this pretentious heading may be that the section's content consists of newly introduced elements, 
whereas the preceding sections explain the use of well-established elements.

### differentiate between visible marks of transpositions and textual transpositions  
* section: 11.3.4.5 Transpositions

The section has a strong focus on visible marks (e.g., numbers). 
While it is true that these often indicate transpositions, it is also true that revisions may visibly look like additions and deletions, 
but may still be viewed as transpositions from a textual point of view.

### rething use of `@change`

In various egXMLs, `@change` is provided on elements `div`, `seg`, `zone`, `line`. 
It should be explained that `@change` may also be used independently of elements the primary function of which is to record the 
structural segmentation or the spatial distribution of the written text.