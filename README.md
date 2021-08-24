# ReAct 

ReAct is a corpus of 1.2k+ carefully curated review comments extracted from ICLR papers reviewed at [OpenReview](https://openreview.net/) for the year [2018](https://openreview.net/group?id=ICLR.cc/2018/Conference), with human annotations to two types of labels. Below is a summary of the dataset statistics: 
  
| Parameters        | Values           |
| ------------- |:-------------:|
| Number of examples     | 1,250 |
| Number of 'Label1' classes   | 2 |
| Number of 'Label' classes   | 7 |
| Average token length of text | ~23 |
| No. of samples w/ 4+ raters agreeing on 'Label1' | 988 (79.04\%) |
| No. of samples w/ 4+ raters agreeing on 'Label2' | 876 (70.08\%) |

The 'Label1' categories are: _actionable_, _non_actionable_.  
The 'Label2' categories are: _agreement_, _disagreement_, _suggestion_, _question_, _shortcoming_, _fact_ and _other_.  


## Data

Our [processed dataset](./processed_data.csv) includes all annotations for a single review comment aggregated over all the turkers. Each row represents an annotation for a single review comment. This file includes the following columns:
```
ReviewId: The unique id of the review.
SentenceId: The unique id of sentence within a review.
Text: The text of the review sentence (or comment).
Label1: The annotated class for 'Label1'.
Label2: The annotated class for 'Label2'.
set: The (train-test) split, a comments belongs to.
```

Our [raw annotated dataset](./raw_annotated_data.csv) includes all annotations as well as metadata on the comments. Each row represents a single rater's annotation for a single review. This file includes an addition column:
```
TurkerId: The unique id of the turker.
```


## Contact 
[Gautam Choudhary](mailto:gautamc@adobe.com), [Natwar Modani](mailto:nmodani@adobe.com), [Nitish Maurya](mailto:nmaurya@adobe.com)

## Citation
This work is accepted at International conference on [Web Information Systems Engineering (WISE), 2021](http://www.wise-conferences.org/2021/index.html).

## Disclaimer
- We are aware that the dataset contains biases and may not be representative of global diversity.
- Potential biases in the data include: inherent biases in OpenReview and user base biases, demographic biases among the annotators as all were native US citizens. These are likely to affect labelling, precision, and recall for a trained model.
- Anyone using this dataset should be aware of these limitations of the dataset and the licensing terms.
  
## License Information
<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />ReAct is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

NOTE: _Please refer [LICENSE](./LICENSE.md) file for detailed information._
