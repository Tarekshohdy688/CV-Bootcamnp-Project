# CV Bootcamp Project

Computer vision exercises and project code, including a modified Darknet fork.

Large model files and supporting folders are stored separately on OneDrive.

## 1. Clone the repository

Clone with submodules to include Darknet:

```bash
git clone --recurse-submodules \
  https://github.com/Tarekshohdy688/CV-Bootcamnp-Project.git

cd CV-Bootcamnp-Project
```

If you already cloned without submodules, run inside the project:

```bash
git submodule update --init --recursive
```

## 2. Download additional folders from OneDrive

The following folders are stored on OneDrive under:

`Google Drive/Projects/CV Bootcamp Project/Vision Learning/`

Download each required folder, extract it if necessary, and place it at the destination below, relative to the cloned repository root.

| Folder | OneDrive download link | Destination inside the project |
|---|---|---|
| Lesson 6_Video_Writing |  | `Vision Learning/Lesson 6_Video_Writing/` |
| Lesson 9_Image_Panorama |  | `Vision Learning/Lesson 9_Image_Panorama/` |
| Lesson 11_Object_Tracking |  | `Vision Learning/Lesson 11_Object_Tracking/` |
| Lesson 13_TF_Object_Detection |  | `Vision Learning/Lesson 13_TF_Object_Detection/` |
| Lesson 14_Pose_Estimation_OpenPose |  | `Vision Learning/Lesson 14_Pose_Estimation_OpenPose/` |

Preserve these folder names and avoid adding an extra nested folder when extracting downloads.

## 3. Set up and run an exercise

Follow the dependency, model, and execution instructions provided with each exercise.

For Darknet build and usage instructions, see [the Darknet README](darknet/README.md). Restore any required model weights before running detection.

## 4. Update the project

Commit or stash local changes in both the main repository and Darknet before updating.

From the repository root:

```bash
git pull --ff-only
git submodule update --init --recursive
```

OneDrive assets must be downloaded separately if they change.

## 5. Save project changes

For changes outside the Darknet submodule:

```bash
git add .
git diff --cached --stat
git commit -m "Update project"
git push
```

Keep downloaded models and other large assets out of Git. Add their destination paths to `.gitignore` before staging changes.

For changes inside Darknet, commit and push them inside that repository first. Then commit and push the updated submodule reference from the main repository.