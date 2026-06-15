### Automation Lab, Sungkyunkwan University

#### GitHub Stats

![](https://img.shields.io/github/downloads/SKKU-AutoLab-VSW/ETSS-08-Data/total.svg?style=for-the-badge)



# Traffic Surveillance Dataset

1. Traffic Surveillance Data Generation capable of producing various environment record on road by using Carla.

  ![gif](attachments/traffic_surveillance_intersection.gif)


2. Real-world traffic surveillance systems

![](attachments/Figure_All_Scenes.jpg)


<!-- MARK: CARLA -->

## I. Using CARLA

<details>

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

</details>


<!-- MARK: TSBOW -->

## II. Real-world System

We are conducting a research to develop a real-world traffic surveillance system.

Comprehensive, annotated dataset for object detection. This dataset consists of over 32 hours of real-world traffic surveillance data across 71 CCTV and an additional color cameras, spanning annual weather conditions ([See Demo Videos](https://skkuautolab.github.io/TSBOW/TSBOW_scenes.html)). The UI for filtering scenes according to each attribute is provided in [Releases: TSBOW-Filter-Scenes_v1.1](https://github.com/SKKUAutoLab/TSBOW/releases/tag/FS_v1.1) on Github repo.

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

```bibtex
@article{Huynh2026TSBOW, 
    title={TSBOW: Traffic Surveillance Benchmark for Occluded Vehicles Under Various Weather Conditions}, 
    volume={40}, 
    url={https://ojs.aaai.org/index.php/AAAI/article/view/37439}, 
    DOI={10.1609/aaai.v40i7.37439}, 
    number={7}, 
    journal={Proceedings of the AAAI Conference on Artificial Intelligence}, 
    author={Huynh, Ngoc Doan-Minh and Tran, Duong Nguyen-Ngoc and Pham, Long Hoang and Tran, Tai Huu-Phuong and Jeon, Hyung-Joon and Nguyen, Huy-Hung and Khac Vu, Duong and Jeon, Hyung-Min and Phan, Son Hong and Pham-Nam Ho, Quoc and Tran, Chi Dai and Khanh, Trinh Le Ba and Jeon, Jae Wook}, 
    year={2026}, 
    month={Mar.}, 
    pages={5239-5247} 
}
```


## IV. License

Both the code and the weights pretrained on the COCO dataset are released under the [Apache 2.0 license](/LICENSE).
