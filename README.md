# Multi-Author-Writing-Style-Analysis-style-change-detection-2023-PAN
Our solution for the task given by PAN at CLEF 2023

## Synopsis
- Task: Given a document, determine at which positions the author changes.
- Input: Reddit comments, combined into documents [data](https://zenodo.org/records/7729178).
- Output: Where does authorship change on the paragraph level.
- Evaluation: F1.
- Submission: TIRA.

## Task
The goal of the style change detection task is to identify text positions within a given multi-author document at which the author switches. Hence, a fundamental question is the following: If multiple authors together have written a text, can we find evidence for this fact; do we have a means to detect variations in the writing style? Answering this question belongs to the most difficult and most interesting challenges in author identification: Style change detection is the only means to detect plagiarism in a document if no comparison texts are given; likewise, style change detection can help to uncover gift authorships, to verify a claimed authorship, or to develop new technology for writing support.

Previous editions of the multi-author writing style analysis task aim at e.g., detecting whether a document is single- or multi-authored (2018), the actual number of authors within a document (2019), whether there was a style change between two consecutive paragraphs (2020, 2021, 2022), and where the actual style changes were located (2021, 2022). In 2022, style changes also had to be detected on the sentence level. The previously used datasets exhibited high topic diversity, which allowed the participants to leverage topic information as a style change signal. In this year's edition of the writing style analysis task, special attention is paid to this issue.

We ask participants to solve the following intrinsic style change detection task: for a given text, find all positions of writing style change on the paragraph-level (i.e., for each pair of consecutive paragraphs, assess whether there was a style change). The simultaneous change of authorship and topic will be carefully controlled and we will provide participants with datasets of three difficulty levels:

- Easy: The paragraphs of a document cover a variety of topics, allowing approaches to make use of topic information to detect authorship changes.
- Medium: The topical variety in a document is small (though still present) forcing the approaches to focus more on style to effectively solve the detection task.
- Hard: All paragraphs in a document are on the same topic.

All documents are provided in English and may contain an arbitrary number of style changes. However, style changes may only occur between paragraphs (i.e., a single paragraph is always authored by a single author and contains no style changes).

[Data](https://zenodo.org/records/7729178)

To develop and then test your algorithms, three datasets including ground truth information are provided (dataset1 for the easy task, dataset2 for the medium task, and dataset3 for the hard task).

Each dataset is split into three parts:

- Training set: Contains 70% of the whole dataset and includes ground truth data. Use this set to develop and train your models.
- Validation set: Contains 15% of the whole dataset and includes ground truth data. Use this set to evaluate and optimize your models.
- Test set: Contains 15% of the whole dataset, no ground truth data is given. This set is used for evaluation.
