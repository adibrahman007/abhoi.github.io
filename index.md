---
title: Amlaan Bhoi
layout: default
---

<script>
function scrambledString(tag, objName, initScrambledString, initScrambledStringIndices) {
	this.tag = tag;
	this.objName = objName;
	this.string = initScrambledString;
	this.indices = initScrambledStringIndices;
	this.rescramble = rescramble;
	this.initAnimatedBubbleSort = initAnimatedBubbleSort;
	this.bubbleSortStep = bubbleSortStep;
	this.bubbleSortBookmark = 0;

	this.rescramble();
	this.tag.innerHTML = this.string + ' <a href="#" onClick="' + this.objName + '.initAnimatedBubbleSort();return false;">unscramble</a>';
}

function rescramble() {
	for (i = 0; i < this.indices.length; i++) {
		indexToMove = Math.floor(Math.random() * (this.indices.length - i));
		charIndexRemoved = this.indices.splice(indexToMove, 1);
		this.indices = this.indices.concat(charIndexRemoved);
		scrambledStringTemp = this.string.substring(0, indexToMove) +
			this.string.substring(indexToMove + 1) +
			this.string.substring(indexToMove, indexToMove + 1);
		this.string = scrambledStringTemp;
	}
}

function initAnimatedBubbleSort() {
	this.interval = setInterval(this.objName + '.bubbleSortStep()', 12);
}

function bubbleSortStep() {		
	if (this.bubbleSortBookmark >= this.indices.length - 1) {
		this.bubbleSortBookmark = 0;
	}
	for (i = this.bubbleSortBookmark; i < this.indices.length - 1; i++) {
		if (i == 0) {
			this.changed = 0;
		}
		if (this.indices[i] > this.indices[i + 1]) {
			this.changed = 1;
			tempIndex = this.indices[i];
			this.indices[i] = this.indices[i + 1];
			this.indices[i + 1] = tempIndex;
			tempArrange = this.string.substring(0, i) +
				this.string.substring(i + 1, i + 2) + 
				this.string.substring(i, i + 1) +
				this.string.substring(i + 2);
			this.string = tempArrange;
			this.tag.innerHTML = this.string;
			this.bubbleSortBookmark = i;
			break;
		}
	}
	this.bubbleSortBookmark = i;
	if (!this.changed) {
		clearInterval(this.interval);
	}
}
</script>

<img src="/images/amlaan_2018.jpg" width="200" align="right" float="right"/>
<h2>Amlaan Bhoi</h2>
Graduate Student<br>
Intel AI Student Ambassador<br><br>
<a href="https://cs.uic.edu">Department of Computer Science</a> <br>
<a href="https://www.uic.edu">University of Illinois at Chicago</a> <br>
851 S Morgan St<br>
Chicago, IL<br>
USA

<!--E-mail: <a href="mailto://abhoi3@uic.edu">abhoi3@uic.edu</a>-->
E-mail: <font id="email" style="display:inline;">
	"bhoi3a@uic.edu "
	<a href="#" onclick="emailScramble.initAnimatedBubbleSort();return false;">unscramble</a>
</font>
<!--<script type="text/javascript">
    emailScramble = new scrambledString(document.getElementById('email'),
        'emailScramble', 'erepc@aahby.etulk.skde',
        [12,13,15,1,8,7,2,5,4,11,18,10,17,3,22,16,6,19,9,14,21,20]);
</script>!-->
<script type="text/javascript">
	emailScramble = new scrambledString(document.getElementById('email'), 'emailScramble', 'duiohce.ua3@bi', [13, 8, 5, 4, 3, 10, 12, 11, 14, 1, 6, 7, 2, 9]);
</script>
<br><br>

### Research Interests

<p align="justify">My current research interests involve spatio-temporal action recognition in videos, object localization in images, and aspect-based sentiment analysis.</p>

### Biography

<p align="justify">Hello, I am Amlaan Bhoi. I am a graduate student of Computer Science in the Department of Computer Science at University of Illinois at Chicago. My research interests are in computer vision, time-series prediction, and data & text mining. I am also an <a href="https://software.intel.com/en-us/ai-academy/ambassadors">Intel AI Student Ambassador</a> through which I share upcoming research on Artificial Intelligence, Machine Learning, & Deep Learning. I love reading machine learning papers on arxiv-sanity and am always keen on learning something new! I graduated from <a href="http://www.amity.edu/">Amity University</a> with a BTech in Computer Science & Engineering in 2017 with First Class honors. Outside classwork, my team won the <a href="https://devpost.com/software/lifeguard-io">"Best Microsoft Hack"</a> at <a href="http://hackharvard.io/">HackHarvard 2017</a> (Cambridge, MA) in Oct 2017. I also dwell around with occasional iOS development and Apple's ARKit to develop augmented reality experiences. Feel free to contact me!</p>

### Current Coursework

- Spring 2018
  - [Advanced Machine Learning](https://www.cs.uic.edu/~zhangx/teaching/CS594_Spring2018_Syllabus.pdf)
  - [Data Mining & Text Mining](https://www.cs.uic.edu/~liub/teach/cs583-spring-18/cs583.html)
  - [Introduction to Data Science](http://cs418.cs.uic.edu/)

### Past Coursework

- Fall 2017
	- [Applied Artificial Intelligence](https://www.cs.uic.edu/Piotr)
	- [Virtual and Augmented Reality](https://www.evl.uic.edu/aej/491/)

### Find Me

- LinkedIn: [abhoi](https://www.linkedin.com/in/abhoi)
- Twitter: [amlaanb](https://www.twitter.com/amlaanb)
- Github: [abhoi](https://www.github.com/abhoi)
- Devpost: [abhoi](https://devpost.com/abhoi)

<!--
You can use HTML elements in Markdown, such as the comment element, and they won't be affected by a markdown parser. However, if you create an HTML element in your markdown file, you cannot use markdown syntax within that element's contents.
-->
