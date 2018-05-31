# project_skt
Deskripsi Tugas Akhir Sistem Komputasi Terdistribusi
Terdapat beberapa komponen dari sistem yang akan dibangun antara lain :     
1. Perangkat Sensor Node         
  a. Perangkat ini berperan untuk mengoleksi data hasil pengukuran sensor untuk kemudian dikirimkan ke cloud lewat komponen sensor-to-cloud gateway menggunakan protokol MQTT. Dalam skema MQTT, perangkat ini berperan sebagai publisher.        
  b. Terdiri atas perangkat keras sensor, mikroprocessor dan perangkat komunikasi         
  c. Perangkat sensor node ini harus bisa berkomunikasi dengan komponen Sensor-to-Cloud Gateway.     
2. Sensor-to-Cloud Gateway         
  a. Komponen ini berperan untuk menerima data yang dikirimkan oleh perangkat sensor node untuk kemudian disimpan dalam perangkat Distributed Database.         
  b. Terdiri atas MQTT broker dan subscriber tunggal.         
  c. Komponen ini harus dapat berkomunikasi dengan Distributed Database.     
3. Distributed Database         
  a. Komponen ini berperan untuk penyimpanan data yang diterima oleh komponen Sensor-to-Cloud Gateway secara real time.         
  b. Data yang disimpan pada komponen ini selanjutnya dapat dimasukkan dalam komponen Distributed Storage untuk kemudian diolah oleh komponen Distributed Processing.         
  c. Selain itu, data yang disimpan dapat juga diakses oleh pengguna lewat perantara komponen User-to-Cloud Gateway.     
4. Distributed Storage (Hadoop Distributed File System/HDFS)         
  a. Komponen ini berperan untuk menyimpan data sensor dari komponen Distributed Database.         
  b. Komponen ini diimplementasikan dengan HDFS.         
  c. Data yang disimpan di komponen ini adalah data yang nantinya diolah oleh komponen Distributed Processing.         
  d. Data pada komponen ini diambil secara periodik dari Distributed Database.     
5. Distributed Processing         
  a. Komponen ini berperan untuk mengolah data secara terdistribusi.          
  b. Data yang diolah berasal dari komponen Distributed Storage.         
  c. Hasil pengolahan data kemudian ditulis ke Distributed Database.     
6. User-to- Cloud Gateway         
  a. Komponen ini berperan sebagai perantara antara cloud dan pengguna akhir.         
  b. Aplikasi pengguna mengakses data yang disimpan di cloud menggunakan protokol HTTP berarsitektur Restful Webservice.     
7. Aplikasi Pengguna         
  a. Komponen ini berperan menampilkan data yang disimpan di server.         
  b. Aplikasi pengguna mengakses data di cloud menggunakan protokol HTTP berarsitektur Restful Webservice.         
  c. Aplikasi pengguna berupa aplikasi mobile berbasis Android/iOS.
