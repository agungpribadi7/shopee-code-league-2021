**Ronde 2**

Pada ronde ini, peserta diberi tugas untuk memilih kata mana yang merupakan nama lokasi dan nama jalan. Dataset berisikan 300.000 data, yang mana terdiri dari 2 kolom yaitu raw_addres dan nama_lokasi/nama_jalan. Dataset dapat dilihat pada link berikut: https://drive.google.com/file/d/1-USbn5SRS0SWFLWtN6oLJE4CuI3f7yBJ/view?usp=sharing . Melihat permasalahan tersebut, maka pemakaian teknik NER (Named Entity Recognition) menjadi salah satu pilihan yang tepat karena kita hanya perlu melabeli pada index string keberapa dan berakhir dimana yang merupakan nama lokasi. Pada code yang diberikan pada github ini, akan digunakan framework milik spacy yang mana sudah mendukung NER. Untuk menggunakan framework ini, kita harus mengubah data training menjadi format sebagai berikut:

TRAIN_DATA = [
    ['who is nishanth?', {
        'entities': [(7, 15, 'ORANG')]
    }],
    ['who is kamal khumar?', {
        'entities': [(7, 19, 'ORANG')]
    }],
    ['i like london and berlin.', {
        'entities': [(7, 13, 'LOKASI'), (18, 24, 'LOKASI')]
    ])
]

Pemilihan bahasa pada framework spacy tidaklah memiliki efek, karena kita melakukan training dari awal, bukan menggunakan model pre-trained milik orang lain. Solusi yang diberikan pada code diatas adalah, melabeli yang mana daerah (seperti Jawa timur, kelurahan sawahan, desa A), dan melabeli nama lokasi dan nama tempat. Melabeli informasi seperti rt. 2 rw.3 menjadi ide yang dapat dicoba selanjutnya. Pada code diatas sebenarnya sudah dilabeli informasi rt dan rw namun belum optimal, sehingga informasi tersebut tidak digunakan. Untuk melabeli daerah menjadi tantangan yang susah karena nama daerah bisa terdiri dari 3 kata, 2 kata dan 1 kata dan juga saat mengurus adanya typo pada raw_data. Pada ronde ini, tim kami memperoleh akurasi **63.045%**. Hasil prediksi dapat dilihat pada file prediction.csv
