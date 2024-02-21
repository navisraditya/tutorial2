- Apa saja pesan log yang dicetak pada panel Output?
Pada panel output, pesan yang dicetak adalah "Platform initialized" ketika developer membuka debugger untuk bermain. Dan ketika objek BlueShip berhasil mencapai ObjectiveArea, muncul pesan "Reached Objective!".

- Coba gerakkan landasan ke batas area bawah, lalu gerakkan kembali ke atas hingga hampir menyentuh batas atas. Apa saja pesan log yang dicetak pada panel Output?
Panel Output akan menuliskan pesan "Reached Objective!" setiap kali objek BlueShip berhasil menyentuh ObjectiveArea berapa kali pun.

- Buka scene MainLevel dengan tampilan workspace 2D. Apakah lokasi scene ObjectiveArea memiliki kaitan dengan pesan log yang dicetak pada panel Output pada percobaan sebelumnya?
Ya. Lokasi ObjectiveArea akan sangat berpengaruh terhadap log yang dicetak pada panel Output. Berdasarkan Script `ObjectiveArea.gd`, terlihat bahwa pencetakan pesan "Reached Objective!" hanya akan terjadi ketika terdapat objek yang menyentuh (collision) ObjectiveArea dan bernama BlueShip. Ketika ObjectiveArea dipindahkan dan `BlueShip` tidak berhasil menyentuh ObjectiveArea, maka tidak akan ada pesan yang dicetak.

- Scene BlueShip dan StonePlatform sama-sama memiliki sebuah child node bertipe Sprite. Apa fungsi dari node bertipe Sprite?
Node dengan tipe `Sprite` berfungsi sebagai object yang bisa diaplikasikan `spritesheet` sebagai teksturnya.

- Root node dari scene BlueShip dan StonePlatform menggunakan tipe yang berbeda. BlueShip menggunakan tipe RigidBody2D, sedangkan StonePlatform menggunakan tipe StaticBody2D. Apa perbedaan dari masing-masing tipe node?
Yang membedakan node dengan tipe `StaticBody2D` dengan `RigidBody2D` adalah pada `StaticBody2D` tidak bisa diaplikasikan fisik sehingga seperti namanya, menjadi statik. Berbeda dengan RigidBody2D dimana kita bisa mengaplikasikan fisik pada objek tersebut sehingga bisa memiliki berat dan gaya gravitasinya (atau hal lain).

- Ubah nilai atribut Mass dan Weight pada tipe RigidBody2D secara bebas di scene BlueShip, lalu coba jalankan scene MainLevel. Apa yang terjadi?
Atribut Mass dan Weight akan saling menyesuaikan valuenya. Ketika Saya mengubah value dari kedua atribut itu, BlueShip akan jatuh ke tanah lebih cepat ketika platform tanahnya menjauh dari BlueShip.

- Ubah nilai atribut Disabled pada tipe CollisionShape2D di scene StonePlatform, lalu coba jalankan scene MainLevel. Apa yang terjadi?
Console tidak mencetak pesan apapun ketika pesawat berhasil mencapai ObjectiveArea karena ObjectiveArea dibuat seakan 'tidak ada' karena statusnya yang ditiadakan (disabled).

- Pada scene MainLevel, coba manipulasi atribut Position, Rotation, dan Scale milik node BlueShip secara bebas. Apa yang terjadi pada visualisasi BlueShip di Viewport?
Fungsi dari masing-masing atribut, adalah:
1. Position: mengubah posisi objek pada game menurut sumbu x dan y
2. Rotation: mengubah derajat objek pada game
3. Scale: mengubah ukuran objek


- Pada scene MainLevel, perhatikan nilai atribut Position node PlatformBlue, StonePlatform, dan StonePlatform2. Mengapa nilai Position node StonePlatform dan StonePlatform2 tidak sesuai dengan posisinya di dalam scene (menurut Inspector) namun visualisasinya berada di posisi yang tepat?
