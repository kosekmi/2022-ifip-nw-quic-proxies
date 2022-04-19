# Exploring Proxying QUIC and HTTP/3 for Satellite Communication

Mike Kosek | Hendrik Cech | Vaibhav Bajpai | Jörg Ott  
Technical University of Munich

[IFIP Networking 2022](https://networking.ifip.org/2022/), June 13&ndash;16, 2022.

[Paper Arxiv &rarr;] TBA

---

## Tools

The following tools were developed for our paper

1. SATCOM Emulation Testbed: Testbed enabling reproducible transport as well as application layer measurements over SATCOM networks leveraging OpenSAND (https://github.com/kosekmi/quic-opensand-emulation)
2. SATCOM Evaluation: Visualization of ```SATCOM Emulation Testbed``` emulations (https://github.com/kosekmi/quic-opensand-evaluation)
3. qperf: A performance measurement tool for QUIC which also enables the proxying of QUIC connections  (https://github.com/kosekmi/qperf)

---

## Reproducibility

In order to enable the reproduction of our ﬁndings, we make the raw data of our measurements as well as the analysis scripts and supplementary ﬁles publicly available within this repository.

0. Repository Overview
* The file ```analysis.ipynb``` is the analysis scripts for the ```goodput``` and ```web performance``` measurements
* The folder ```dataset``` contains the datasets which are provided as csv files

1. Dataset Overview
* The files ```goodput_1s_bins.csv``` and ```goodput_100ms_bins.csv``` in the ```dataset``` folder contain the aggregated goodput measurement data in 1s and 100ms bins
* The file ```web_performance.csv``` in the ```dataset``` folder contains the web performance measurement data
* All files contain their respective data over all measurement runs for all tested combinations of orbit (`leo` or `geo`), transport protocol (`quic` or `tcp`), Performance Enhancing Proxy (`true` or `false`), initial window (`10,10,10,10` or `10,100,100,10`), and packet loss rate (`0` or `0.01` or `0.1` or `1` %)

2. Preparations
* Clone this repository to a machine running ```Jupyter Notebook``` or ```JupyterLab```

3. Goodput
* Run the Jupyter Notebook ```goodput.ipynb```

4. Web Performance
* Run the Jupyter Notebook ```web_performance.ipynb```

---

## Contact

Please feel welcome to contact the authors for further details.

* Mike Kosek (kosek@in.tum.de) (corresponding author)
* Hendrik Cech (cech@in.tum.de)
* Vaibhav Bajpai (bajpai@cispa.de)
* Jörg Ott (ott@in.tum.de)