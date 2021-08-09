# create-and-predict-models.h5-using-CNN
predict an image from the dataset that we have prepared and saved in model.h5 format so that it is ready to be used for your needs


here I use Colab or jupyter

# dataset 
siapkan dataset yang Anda inginkan di sini saya memiliki 8 folder gambar pada setiap tes dan train
(prepare the dataset you want here i have 8 image folder on each test and train)

# Perbanyak Dataset Sampel (Expand Sample Dataset)
dimana setiap gambar pada train dan test akan kita gandakan sebanyak 100x dan kita ubah ukuran, rotasi dan ukuran zoom (where each image on the train and test will be multiplied by 100x and we will change the size, rotation and zoom size)
setelah kita gandakan kemudian file asli pada train akan kita hapus
(after we duplicate then the original file on the train we will delete)

# Tahap Pelatihan / Training Phase
menggunakan 2 layer dengan filter berukuran 64 dan 32.  kernel size 3x3. aktifasi sofmax dan compile menggunakan categorical_crossentropy
(using 2 layers with filters measuring 64 and 32. kernel size 3x3. activate softmax and compile using categorical_crossentropy)
"model.add(Dense(units = 8, activation = 'softmax'))" units = 8, i have 8 categories replace with your needs

# save model
use 
> model.save('model.h5')
