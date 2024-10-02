# COnversational DYnamics Model (CODYM)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

The CODYM is a Markov-based model of conversational dynamics based on the binarized length of speaker turns. CODYM analysis offers a robust methodology for examining information flow between conversational participants in a variety of contexts. 

## Background
The nodes of a *k*-order CODYM represent the binarized lengths of the previous *k* turns. Edges of the model represent the length of the current turn. Models are populated with the frequency of occurrence of each state/transition in all turns in a corpus (or any specified subset thereof). In the 2-order and 3-order models below, **S** represents a short turn and **L** represents a long turn.

![CODYM example](img/CODYMs.png "CODYM example")
|:--:| 
| *Example of un-populated 2nd- and 3rd-order CODYMs* |

The following scripts can be used to populate a CODYM model and draw the state space diagram for 2- and 3-order models, for both standard and "difference" CODYMS. For demonstration purposes, two examples are included. The first example (`CODYM_example1.py`) comes from our forthcoming paper [1], using the anonymized dataset contained in the supporting information, and depicts conversations between patients with advanced cancer and palliative care clinicians. This "difference" CODYM shows how information flow patterns vary between patient turns where distressing emotion was expressed vs. those conversations without these emotions detected. 

![CODYM example](img/emo_diff_codym.png "Difference CODYM between patient turns in conversations with expressed emotion and without")
|:--:| 
| *Difference CODYM between patient turns in conversations with expressed emotion and without* |

The second example (`CODYM_example2.py`) creates a CODYM model for the Supreme Court Corpus, as distributed from Cornell's [ConvoKit](https://convokit.cornell.edu/) Conversation Analysis Toolkit. This script will require installing ConvoKit, which can be done [here](https://convokit.cornell.edu/). This script produces 2nd- (not pictured here) and 3rd-order CODYMs representing the average for all 553 conversations in the Supreme Court Corpus with at least 20 utterances.

![CODYM example](img/CODYM_example_plot.png "Normative CODYM of the Supreme Court Corpus")
|:--:| 
| *Normative CODYM of the Supreme Court Corpus* |

## Install
You can run this Python script locally

## Usage
This code is still very much in development, and comes with no guarantees. For more information on CODYM analysis, how to interpret a CODYM model, and an example application in the study of serious illness communication, see [our paper in PLOS ONE](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0253124). Extended analytical techniques using CODYM analysis are included in our [preprint](https://arxiv.org/abs/2010.05164).

## Contributing
Pull Requests are accepted, please review the [the contributing file](CONTRIBUTING.md)!

## License

[Apache-2.0 license](../LICENSE)

## Citation
Clarfeld L, Gramling R, Rizzo D, Eppstein M.  A general model of conversational dynamics with application in serious illness communication. PLoS One. 2021. Jul 1;16(7):e0253124 [https://doi.org/10.1371/journal.pone.0253124](https://doi.org/10.1371/journal.pone.0253124)

