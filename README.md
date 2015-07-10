# Medieval
### Segmentations on MICCAI 2009 LV Grand Challenge  

#### Organization of the directory Segmentations-LV:  
45 subdirectories, one per subject.  
Naming of subject is similar to the MICCAI 2009 LV Grand Challenge database: SC-\*-XY   
(XY being two digits, \* corresponding to subject subcategory: N, HYP, HF-I, HF-NI). 

For each subject, there are eight subdirectories corresponding to eight segmentation methods: method01, method02, method03, method04, method05, method06, method07, method08.   
The eight methods are described in the paper entitled " Improved estimation of cardiac function parameters using a combination of independent automated segmentation results in cardiovascular magnetic resonance imaging" and presently submitted to Plos One.  
Inside each subdirectory there are two files: Cav_seg_SC-\*-XY_methode0Z (a text file describing the binary data) and Cav_seg_SC-\*-XY_methode0Z.dat.gz (gzip of the binary data).

#### Organization of the directory Segmentations-Epicardium-LV:  
The organization is similar to the directory Segmentations-LV
Regions are defined inside the epicardial contours for end-diastolic images
For each subject, there are seven subdirectories corresponding to seven segmentation methods: method01, method02, method03, method04, method05, method06, method08.   
Inside each subdirectory there are two files: Seg_SC-\*-XY_methode0Z (a text file describing the binary data) and Seg_SC-\*-XY_methode0Z.dat.gz (gzip of the binary data).

#### Example of files:   
The text file Cav_seg_SC-HF-I-04_methode01 describes the 4D dataset corresponding to the labeling of the left ventricle region (defined inside the endocardial contours) of subject SC-HF-I-04 by method01.

!width := 256             (First dimension of image slice)  
!height := 256            (Second dimension of image slice)  
!slice_number := 10       (Number of slices for this specific dataset)  
!phase_number := 20       (Number of time samples for this 4D data set)  
!number format := unsigned integer (Format of label : unsigned integer)  
!number of bytes per pixel := 1    (Format of label : one byte per element)  
!filenumber := 1          (Format of 4D data set : only one file)  
!name of data file[1] := Cav_seg_SC-HF-I-04_methode01.dat (Name of the data file)  
!interslice_distance:= 8  (Slice thickness in mm)
!width_resolution:= 1.289100 (Pixel size in mm)
!height_resolution:= 1.289100 (Pixel size in mm)

When decompressed, Cav_seg_SC-HF-I-04_methode01.dat is a 4D dataset (size: 256x256x10x20 voxels) of unsigned bytes with three possible values: 
* 0 for background
* 1 for left ventricle (inside endocardial contours)
* 255 for unsegmented slices

NB The two label values 0 or 1 occur only for segmented slices.


