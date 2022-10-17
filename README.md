# Basic Algorithm for Risk-Based Authentication

> Basic implementation of the [Risk-Based Authentication (RBA)] algorithm by [Freeman et al. (2016)] in Python 3. Optimized for performance and edge cases.

[Risk-Based Authentication (RBA)]: https://riskbasedauthentication.org/
[Freeman et al. (2016)]: https://doi.org/10.14722/ndss.2016.23240

## Table of Contents

- [About](#about)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Authors](#authors)
- [License](#license)

## About

### Background

Risk-Based Authentication (RBA) is an approach to improve account security on websites without forcing users to use Two-Factor Authentication (2FA). Users consider RBA more usable than comparable 2FA methods. This technology is getting more and more important, as it is recommended by the NIST (USA), NCSC (UK), and ACSC (AU), and is also subject of an executive order by President Biden. Also, big online services like Google, Amazon, Facebook, and LinkedIn use RBA.

During login, RBA estimates a risk score based on features describing the login behavior. On a low risk (e.g., same device as always), the website grants access. On a medium risk (e.g., unknown device), the website asks for additional information to prove the claimed identity.

### Repository

This repository provides a Jupyter Notebook containing an algorithm to calculate the RBA risk score. The algorithm was originally proposed in [Freeman et al. (2016)]. We further optimized it for performance on large distributed systems like a supercomputer (high-performance computing, HPC). We also considered some edge cases that were not described in the original publication.

The implementation was used in the following publications to analyze RBA characteristics in practice:

- [Pump Up Password Security! Evaluating and Enhancing Risk-Based Authentication on a Real-World Large-Scale Online Service] (2022)<br />
  _Stephan Wiefling, Paul René Jørgensen, Sigurd Thunem, and Luigi Lo Iacono_.<br />
  _ACM Transactions on Privacy and Security_

- [Privacy Considerations for Risk-Based Authentication Systems] (2022)<br />
  _Stephan Wiefling, Jan Tolsdorf, and Luigi Lo Iacono_.<br>
  _2021 International Workshop on Privacy Engineering (IWPE '21), co-located with IEEE EuroS&P '21_

- [What's in Score for Website Users: A Data-Driven Long-Term Study on Risk-Based Authentication Characteristics] (2021)<br />
  _Stephan Wiefling, Markus Dürmuth, and Luigi Lo Iacono_<br />
  25th International Conference on Financial Cryptography and Data Security (FC '21)

[Pump Up Password Security! Evaluating and Enhancing Risk-Based Authentication on a Real-World Large-Scale Online Service]: https://doi.org/10.1145/3546069

[Privacy Considerations for Risk-Based Authentication Systems]: https://nbn-resolving.org/urn:nbn:de:hbz:1044-opus-58417

[What's in Score for Website Users: A Data-Driven Long-Term Study on Risk-Based Authentication Characteristics]: https://pub.h-brs.de/files/5956/Wiefling2021_WhatsInScoreForWebsiteUsers-Postproceedings.pdf

## Getting Started

The following steps should help you to set up the environment to open the Jupyter Notebook and run the algorithm.

### Installing

To run this notebook, you need *JupyterLab* or compatible software, together with *Python 3* and *pandas*.

We recommend to install [Anaconda]. The Anaconda installer should install JupyterLab and Python3 with pandas automatically in a new environment, so you're ready to go.

[Anaconda]: https://www.anaconda.com/

### Open Project

1. Open Anaconda Navigator and launch JupyterLab.
2. Open `rba-algorithm.ipynb` and save it as a copy, so that JupyterLab trusts the notebook.
3. Run the code or edit it on your own.

## Contributing

Feel free to submit your pull request to this repository. Please follow the [contribution guide] to do so.

[contribution guide]: ./CONTRIBUTING.md

## Authors

- Stephan Wiefling

## License

&copy; 2022 Stephan Wiefling / [Data and Application Security Group](https://das.h-brs.de)

The code in this repository is licensed under the MIT License ([LICENSE](LICENSE)).
