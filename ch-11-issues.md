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

## introductory comment about document-focused and text-focused transcription

### current version

```xml
   <p>This chapter defines a module intended for use in the representation of primary sources, such
      as manuscripts or other written materials. Section <ptr target="#PHFAX"/> provides elements
      for handling digitally-encoded images of such materials. This module may also be useful in the
      preparation of critical editions, but the module defined here is distinct from that defined in
      chapter <ptr target="#TC"/>, and may be used independently of it. Detailed metadata relating
      to primary sources of any kind may be recorded using the elements defined by the manuscript
      description module discussed in chapter <ptr target="#MS"/>, but again the present module may
      be used independently if such data is not required. </p>
   <!-- following para may need revision? -->
   <!-- p>It should be noted that, as elsewhere in these Guidelines,  this
chapter places more emphasis on the problems of representing the
textual components of a document than on those relating to the
description of the document's physical characteristics such as the
carrier medium or physical construction. These aspects, of particular
importance in codicology and the bibliographic study of incunables,
are touched on in the chapter on Manuscript Description (<ptr target="#MS"/>) and also form the subject of ongoing work in the TEI
Physical Bibliography workgroup.</p-->
```
(https://github.com/TEIC/TEI/blob/78696cddc07ce1b3285417202b619857e611aa2d/P5/Source/Guidelines/en/PH-PrimarySources.xml#L13)

### hints
See Raff's comment https://github.com/TEIC/TEI/issues/1427#issuecomment-214744864.

- [ ] summarize the concerns raised in the comments
- [ ] draft 4 or 5 sentences to add to the introduction to the chapter

### revision draft
This chapter defines a module intended for use in the representation of primary sources as facsimiles and transcription.
<small>Detailed bibliographical and physical metadata about such source documents may be recorded using the manuscript description module (chapter 10). When multiple versions of one and the same text are to involved, chapter 12 Critical Apparatus may be used to record variants across source documents.</small>

The TEI offers two basic approaches for the encoding of such materials, one that views the intellectual units of communication as the 
fundamental hierarchy and one that takes as its primary concern the physical arrangement of text on the inscribed surface. 
In the discussion that follows, these two approaches are, for the sake of convenience, sometimes termed "text-focused" and 
"document-focused." 
This usage is not meant to imply a rigorous theoretical distinction between "text" and "document," however. 
Nor does the emphasis in the current chapter on the second approach imply a preference for that approach. 
Those whose goals are better served by the latter approach are advised to use the guidelines from the current chapter in conjunction 
with those found in other chapters, especially _________

## rotation center for `@rotate`
Details may be added by @JSchaeuble.

## `@ulx` etc. on `zone`
Details may be added by @JSchaeuble.