## H36_3D_Pose_Estimation_Simple_Baseline

This is the code for the paper

Julieta Martinez, Rayat Hossain, Javier Romero, James J. Little.
_A simple yet effective baseline for 3d human pose estimation._
In ICCV, 2017. https://arxiv.org/pdf/1705.03098.pdf.

Changes have been made to run the code on Tensorflow 2.x

## Dependencies

* Python ≥ 3.8
* [cdflib](https://github.com/MAVENSDC/cdflib)
* [tensorflow](https://www.tensorflow.org/) 2.0 or later

## Get the data

Go to http://vision.imar.ro/human3.6m/, log in, and download the `D3 Positions` files for subjects `[1, 5, 6, 7, 8, 9, 11]`,
and put them under the folder `data/h36m`. Your directory structure should look like this

```bash
src/
README.md
LICENCE
...
data/
  └── h36m/
    ├── Poses_D3_Positions_S1.tgz
    ├── Poses_D3_Positions_S11.tgz
    ├── Poses_D3_Positions_S5.tgz
    ├── Poses_D3_Positions_S6.tgz
    ├── Poses_D3_Positions_S7.tgz
    └── Poses_D3_Positions_S9.tgz
```

Now, move to the data folder, and uncompress all the data
Finally, download the `code-v1.2.zip` file, unzip it, and copy the `metadata.xml` file under `data/h36m/`

Now, your data directory will contain the xml file and the folders for respective subjects

```bash
data/
  └── h36m/
    ├── metadata.xml
    ├── S1/
    ├── S11/
    ├── S5/
    ├── S6/
    ├── S7/
    └── S9/

```

There is one little fix we need to run for the data to have consistent names:

```bash
mv h36m/S1/MyPoseFeatures/D3_Positions/TakingPhoto.cdf \
   h36m/S1/MyPoseFeatures/D3_Positions/Photo.cdf

mv h36m/S1/MyPoseFeatures/D3_Positions/TakingPhoto\ 1.cdf \
   h36m/S1/MyPoseFeatures/D3_Positions/Photo\ 1.cdf

mv h36m/S1/MyPoseFeatures/D3_Positions/WalkingDog.cdf \
   h36m/S1/MyPoseFeatures/D3_Positions/WalkDog.cdf

mv h36m/S1/MyPoseFeatures/D3_Positions/WalkingDog\ 1.cdf \
   h36m/S1/MyPoseFeatures/D3_Positions/WalkDog\ 1.cdf
```

## Scripts
All scripts used are in script.txt

