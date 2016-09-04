## Original Twitter Data

### 1. Overview

The original Twitter data can be visited at [Dataset-UDI-TwitterCrawl-Aug2012](https://wiki.illinois.edu//wiki/display/forward/Dataset-UDI-TwitterCrawl-Aug2012).

This dataset is a subset of Twitter. It contains 284 million following relationships, 3 million user profiles and 50 million tweets. The dataset was collected at May 2011. 

Visit the link above for more information about the raw data. 

> Great thanks to Rui Li & et al. for providing this Twitter data.

### 2. Experiment Data

    ~/JOS_data
         |---> /experiment
         |           |---> /summarization
         |           |                   /20110125obama
         |           |                   ...
         |           |                   /20110519obama
         |           |---> /tp_detection
         |                             /iPad_all
         |                             /Microsoft_all
         |                             /Obama_all
         |---> /expert
         |          |---> /summarization
         |          |                   /20110125obama-duan
         |          |                   ...
         |          |                   /20110519obama-wang
         |          |---> /tp_detection
         |                             /ipad.eval1
         |                             ...
         |                             /obama.eval3
         |---> /README.md

### 3. Data Case Example

1) The **expert time-points** look like:

    20110311 20110420 20110607 20110302 20110505 20110531 20110215 20110223 20110114 20110119

where 10 most important dates are ranked from "most important" to "less important", and "20110311" means "March, 11, year of 2011". There're 3 expert corpus for each keyword, totally 9 expert corpus for 3 keywords.

2) The **expert summary** looks like:

    paul ryan hit a home run and decimated just about every argument obama made.  that's how you give a speech.
    so far, obama has praise muslims, illegal immigrants, and unions--the three biggest problems facing the united states.
    we commend  and the rsc for de-funding obamacare in their spending reduction act!  
    president obama co-opted much of the gop agenda in his speech. now let's see if he'll walk the talk.  ...
    obama: "we are a nation of google and facebook" - 
    obama in  asks congress to make permanent 4-year college tax credit 
    obama gives a major shoutout to  repeal and calls for college campuses to welcome rotc and military recruiters.
    obama in  says he's "willing to look at" medical malpractice reform 
    obama on clean energy, biofuels, cutting oil subsidies, complicated salmon management, and high speed rail 
    members of congress less keen on obama's proposal to freeze domestic spending for next five years 

every expert were asked to select about 10 sentences from given Twitter set of an sub-event. There're 3 expert summaries for each sub-event, totally 12 summaries for 4 sub-events

3) The **experiment data for hot sub-event time-points detection** looks like:

    Text: RT  Appearing on  from 10:40 to 11:00 a.m. 2day 2 discuss Obama, 2012 and Common 
    Time: Fri May 13 08:55:15 CDT 2011
    ...
    ...
    ...
    Text: "You can be the generation that ends HIV/AIDS in our time," said first lady Michelle Obama. Amazing speach! This... 
    Time: Wed Jun 22 12:55:14 CDT 2011

where every first line is the Twitter text, the second line is the timestamp this tweet being posted.

4) The **experiment data for sub-event summary** looks like:

    ***
    userid:100072535
    Text: RT  President Obama in  speech: 'This is our generation's Sputnik moment' - more updates, images at Breaking News htt ...
    URL: 
    Time: Tue Jan 25 20:31:43 CST 2011
    RetCount: 31
    ***

where the tags mean:

<table>
<tbody>
<tr><td><b>Tags</b></td><td><b>Descriptions</b></td></tr>
<tr><td>***</td><td>Unit Separator</td></tr>
<tr><td>userid</td><td>unique ID of the user who post this tweet</td></tr>
<tr><td>Text</td><td>tweet text</td></tr>
<tr><td>URL</td><td>url links in this tweet (if exists)</td></tr>
<tr><td>Time</td><td>timestamp this tweet being posted</td></tr>
<tr><td>RetCount</td><td>how many times this tweet has been retweeted</td></tr>
<tr><td>***</td><td>Unit Separator</td></tr>
</tbody>
</table>

## Tools

+ **MEAD**
 + [Download](http://www.summarization.com/mead/)
 + [Documentation](http://www.summarization.com/mead/documentation/meaddoc.pdf)

+ **Wavelet Analysis**
 + [Documentation](https://en.wikipedia.org/wiki/Wavelet)

## Evaluation

+ **MAP**
 + [Mean Average Precision](https://www.kaggle.com/wiki/MeanAveragePrecision)
 + [Evaluation of ranked retrieval results](http://nlp.stanford.edu/IR-book/html/htmledition/evaluation-of-ranked-retrieval-results-1.html)

+ **ROUGE**
 + [ROUGE: A Package for Automatic Evaluation of Summaries
](http://www.aclweb.org/anthology/W04-1013)
 + [Download](http://www.isi.edu/licensed-sw/see/rouge/)

## Citation

**EN:**

> Yu GC, He RF, Liu Y, Dang JW. Context Based Model for Temporal Twitter Summarization. Ruan Jian Xue Bao/Journal of Software, 2016 (in Chinese). http://www.jos.org.cn/1000-9825/0000.htm

**CN:**

> 于广川,贺瑞芳,刘洋,党建武. 融合语境分析的时序推特摘要方法.软件学报. http://www.jos.org.cn/1000-9825/ 0000.htm

