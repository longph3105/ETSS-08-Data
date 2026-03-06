### Automation Lab, Sungkyunkwan University

#### GitHub Stats

![](https://img.shields.io/github/downloads/SKKU-AutoLab-VSW/ETSS-08-Data/total.svg?style=for-the-badge)



# Traffic Surveillance Dataset

1. Traffic Surveillance Data Generation capable of producing various environment record on road by using Carla.

  ![gif](attachments/traffic_surveillance_intersection.gif)


2. Real-world traffic surveillance systems

![](attachments/Figure_All_Scenes.jpg)


## I. Using CARLA

<details open>

  <summary>Building CARLA, Instruction, and samples</summary>

  ### 1. Building CARLA

  Use `git clone` or download the project from [CARLA Github][carlagithublink].

  Then follow the instruction at [How to build on Linux][buildlinuxlink] or [How to build on Windows][buildwindowslink].

  The Linux build needs for an UE patch to solve some visualization issues regarding Vulkan. Those already working with a Linux build should insta


  ### 2. Instruction the patch and make the UE build again using the following commands.

  ```sh
  # Download and install the UE patch  
  cd ~/UnrealEngine_4.24
  wget https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/UE_Patch/430667-13636743-patch.txt ~/430667-13636743-patch.txt
  patch --strip=4 < ~/430667-13636743-patch.txt

  # Build UE
  ./Setup.sh && ./GenerateProjectFiles.sh && make
  ```

  [carlagithublink]: https://github.com/carla-simulator/carla
  [buildlinuxlink]: https://carla.readthedocs.io/en/latest/build_linux/
  [buildwindowslink]: https://carla.readthedocs.io/en/latest/build_windows/
  

  Please refer to [INSTRUCTION.md](DataGeneration-CARLA/Instruction.md) for how to use.


  ### 3. Sample

  Please go to this repository for [Realistic-Traffic-Surveillance Generated Sample](https://github.com/SKKU-AutoLab-VSW/Realistic-Traffic-Surveillance_GeneratedSample)

</details open>


## II. Real-world System

We are conducting a research to develop a real-world traffic surveillance system.

Please go to [TSBOW-dataset](https://github.com/SKKUAutoLab/TSBOW) repository or [TSBOW-website](https://skkuautolab.github.io/TSBOW/) for more details.


## III. Citation 

If you find our work helpful for your research, please consider citing the following BibTeX entry.

1. Data Generation using Carla

```bibtex
@misc{AutoLab-Dataset-CARLA,
  author = {Automation Laboratory},
  license = {Apache-2.0},
  title = {Traffic Surveillance Dataset},
  howpublished = {https://github.com/SKKUAutoLab/ETSS-08-Data},
  year = {2025},
  note = {Data Generation using Carla}
}
```

2. Real-World System

We will update the citation again after the AAAI-26 proceedings publication.

```bibtex
@misc{huynh2026tsbowtrafficsurveillancebenchmark,
      title={TSBOW: Traffic Surveillance Benchmark for Occluded Vehicles Under Various Weather Conditions}, 
      author={Ngoc Doan-Minh Huynh and Duong Nguyen-Ngoc Tran and Long Hoang Pham and Tai Huu-Phuong Tran and Hyung-Joon Jeon and Huy-Hung Nguyen and Duong Khac Vu and Hyung-Min Jeon and Son Hong Phan and Quoc Pham-Nam Ho and Chi Dai Tran and Trinh Le Ba Khanh and Jae Wook Jeon},
      year={2026},
      eprint={2602.05414},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2602.05414}, 
}
```


## IV. License

Both the code and the weights pretrained on the COCO dataset are released under the [Apache 2.0 license](/LICENSE).