# Intel® IoT Getting Started Docs Contribution Guide

We welcome pull requests and bug reports on these docs.

**For minor typos and edits:** Fork this repo, make your edits on your local computer or [directly on Github](https://help.github.com/articles/editing-files-in-your-repository/), then [submit a PR](https://help.github.com/articles/using-pull-requests/).

**For larger updates:** Start a ticket in the Github issue tracker to let us know what you are working on. This will allow others to provide feedback as well as coordinate contribution efforts.

## Branches

### branch: master

[github.com/intel-iot-roadshow/getting-started-guides](https://github.com/intel-iot-roadshow/getting-started-guides)

Currently straight Markdown-formatted docs. This is where everyone is editing content and can continue to edit content for now. After the dust settles from the LA Roadshow, this branch will probably be shut down and replaced by the "jekyll" branch. 

### branch: jekyll

[github.com/intel-iot-roadshow/getting-started-guides/tree/jekyll](https://github.com/intel-iot-roadshow/getting-started-guides/tree/jekyll)

See [the branch's README](https://github.com/intel-iot-roadshow/getting-started-guides/blob/jekyll/README.md) for how to preview/build content in this branch.

Note: Once I'm fully done with the content sweep, when we make edits to content, we'll have to update the .md files on BOTH 'master' and 'jekyll' branches. I will let you know when/if this needs to happen but I plan to finish the sweep in the next couple of hours.

### branch: html

[github.com/intel-iot-roadshow/getting-started-guides/tree/html](https://github.com/intel-iot-roadshow/getting-started-guides/tree/html)

THIS IS THE BRANCH THAT WILL BE PUT ON USB KEYS. Static files need to be generated form the 'jekyll' branch. See [the branch's README](https://github.com/intel-iot-roadshow/getting-started-guides/blob/html/README.md) for details on running a local web server to view files.

### branch: gh-pages

[github.com/intel-iot-roadshow/getting-started-guides/tree/html](https://github.com/intel-iot-roadshow/getting-started-guides/tree/html)

Github's built in web server for viewing html files: [https://github.com/intel-iot-roadshow/getting-started-guides/tree/gh-pages](https://github.com/intel-iot-roadshow/getting-started-guides/tree/gh-pages). Feel free to send anyone to this url if they are unable to get the USB key files working. Static files need to be generated form the 'jekyll' branch.


## Style Guide

Many of these docs originated as a Google Doc and PDFs. Some of the points in the [original style guide](https://docs.google.com/document/d/1C-UeNNmMEX-wXcJLTrflbCm_L93bq3g0aa2CTHNf6Aw/preview) may not apply to these Markdown docs but still worth a read. 

### Language

* Explain what **and why** but keep it short and sweet.
* Keep "skimmability" in mind at all times. No one reads every word so make important ones **jump** out using bold or italics.
* Use numbered lists and bullet points. Avoid rambling in paragraphs.
* Make the content impersonal, gender neutral, and action-oriented -- this content is meant to be re-used across different mediums and platforms. Jokes do not translate well.

### Images

* **Show, don't tell**: Add screenshots and/or photos for clarity.
* However, having said that, even when using an image **do not leave out text-based instructions** for accessibility reasons.
* For ease of translation, do not put text overlays in images. Use numbered or lettered captions, if necessary.
* To show an action, put together a before & after montage or consider an [animated gif](https://github.com/vvo/gifify).
* Use #ff8c00 orange for callout arrows and circles. (Avoid #e21f20 red callouts unless it is actually an indication of an error or danger.)
* Crop images to bring extra attention to the important area and to save space — but make sure to keep context (ie. don't overcrop).
* Compress your images before adding to the repo. Try [TinyPNG](https://tinypng.com/) or similiar tools.

### Command line input

* Make commands that a reader needs to type jump out and easy to copy/paste by using a single backtick (\`) or [triple backticks](https://help.github.com/articles/github-flavored-markdown/#fenced-code-blocks) (```) for multiple lines.

### Code samples

* Make code easy to copy/paste -- use [triple backticks](https://help.github.com/articles/github-flavored-markdown/#fenced-code-blocks) (```) for code blocks.
* 2 spaces (not tabs)

## Possible additions

### Want to add a new breakout board?

1. Add it to the main [README.md](README.md)
2. Create a sub-folder in the [assembly folder](/assembly) for the new board
  * Create a doc for **assembly**
  * And another **connecting_cables** doc that is more like an appendix
3. Create an end-to-end guide in the [START_HERE folder](START_HERE/) for some basic Hello World app

### Want to add a new sensor kit?

1. Create a sub-folder in the [sensor examples folder](/sensor_examples) for the new kit
  * Create an **intro** doc
  * Put code samples into a language specific folder (since there will likely be different screenshots/gifs/videos for different languages)

---

## Questions or concerns?

Please file a ticket in the Github issue tracker. The Intel® IoT team want these to be the best docs out there so don't be shy. Please follow the [Contributor Code of Conduct](CODE_OF_CONDUCT.md)
