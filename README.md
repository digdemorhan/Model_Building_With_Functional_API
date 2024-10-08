# Model_Building_With_Functional_API

# Projenin Ana Teması
Bu proje, California konut fiyatlarının tahmin edilmesi amacıyla oluşturulmuş bir derin öğrenme modelidir. Veriler, California'nın çeşitli bölgelerindeki konut bilgilerini içermektedir. Model, farklı giriş katmanları kullanarak çoklu çıkışlar elde edebilecek şekilde tasarlanmıştır.

# Kurulum
Proje için gerekli kütüphanelerin yüklenmesi gerekmektedir. Aşağıdaki komutları kullanarak gerekli kütüphaneleri yükleyebilirsiniz:
pip install scikit-learn tensorflow pandas

# Modelin Mimarisi 
Bu projede, Functional API kullanılarak iki farklı girdi katmanı olan bir sinir ağı modeli inşa edilmiştir. Modelin mimarisi aşağıdaki gibidir:
<ul>
  <li><b>Input Layer:</b>"input_wide" 5, "input_deep" 6 özelliği alır.</li>
  <li><b>Normalization Layer:</b>"norm_layer_wide" ve "norm_layer_deep" ile girdiler normalleştirilmiştir.</li>
  <li><b>Hidden Layer:</b>İki adet gizli katman vardır; her biri 30 nörondan oluşur ve ReLU aktivasyon fonksiyonu kullanır.</li>
  <li><b>Output Layer:</b>Modelin ana çıktısı ve yardımcı çıktısı olmak üzere iki ayrı çıktı katmanı bulunmaktadır.</li>
</ul>

# Modelin Kurulumu ve Eğitimi
Model, eğitim verileri üzerinde eğitilmiştir. Normalizasyon işlemi sonrası model, belirli bir sayıda epoch boyunca eğitim yapılmıştır. Eğitim sırasında %20'lik bir doğrulama seti kullanılmıştır.
<ul>
  <li><b>Veri Setinin Yüklenmesi:</b>"fetch_california_housing" kullanılarak konut verisi yüklenmiştir. Veri seti eğitim ve test verilerine ayrılmıştır.</li>
  <li><b>Modelin Kurulması:</b>TensorFlow kullanılarak model oluşturulmuştur. Normalizasyon katmanı ve iki gizli katman içeren bir yapıya sahiptir.</li>
  <li><b>Sinir Ağının İnşası:</b>Girdi katmanı oluşturulmuş ve veriler normalizasyon katmanından geçirilmiştir. Gizli katmanların çıktıları birleştirilerek çıktı katmanı oluşturulmuştur.</li>
  <li><b>Modelin Compile Edilmesi:</b>"Adam" optimizasyon algoritması kullanılarak model derlenmiştir. Kayıp fonksiyonu olarak "Mean Squared Error (MSE)" seçilmiştir.</li>
</ul>

# Sonuçlar
Model, test verileri üzerinde değerlendirilmiş ve performansı ölçülmüştür. Tahminler, gerçek değerlerle karşılaştırılarak analiz edilmiştir. Modelin değerlendirme sonuçları ve tahmin sonuçları ayrıntılı olarak gösterilmiştir.

----
----

# Main Theme of the Project
This project is a deep learning model for predicting California house prices. The data includes housing information from various regions of California. The model is designed to obtain multiple outputs using different input layers.

# Installation
The libraries required for the project need to be installed. You can install the necessary libraries using the commands below:
pip install scikit-learn tensorflow pandas

# Architecture of the Model
In this project, a neural network model with two different input layers is built using the Functional API. The architecture of the model is as follows:
<ul>
  <li><b>Input Layer:</b>“input_wide” takes property 5, ‘input_deep’ takes property 6.</li>
  <li><b>Normalization Layer:</b>Inputs are normalized with “norm_layer_wide” and “norm_layer_deep”.</li>
  <li><b>Hidden Layer:</b>There are two hidden layers, each consisting of 30 neurons and using the ReLU activation function.</li>
  <li><b>Output Layer:</b>The model has two output layers, the main output and the auxiliary output.</li>
</ul>

# Model Setup and Training
The model is trained on the training data. After normalization, the model was trained for a certain number of epochs. A validation set of 20% was used during training.
<ul>
  <li><b>Loading the Data Set:</b>The housing data was loaded using “fetch_california_housing”. The dataset is divided into training and test data.</li>
  <li><b>Establishment of the Model:</b>The model was created using TensorFlow. It has a structure including a normalization layer and two hidden layers.</li>
  <li><b>Neural Network Construction:</b>The input layer is created and the data is passed through the normalization layer. The outputs of the hidden layers are combined to form the output layer.</li>
  <li><b>Compile the Model:</b>The model was compiled using the “Adam” optimization algorithm. “Mean Squared Error (MSE)” was chosen as the loss function.</li>
</ul>

# Results
The model was evaluated on test data and its performance was measured. The predictions are analyzed by comparing them with the actual values. The evaluation results and prediction results of the model are shown in detail.
