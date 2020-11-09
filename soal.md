## Prelude
Masih ingat tentang online learning yang pernah kalian buat kan?

Sekarang saatnya kita mencoba lagi yah untuk membuat aplikasi Online Learning,
namun dengan menggunakan sequelize.

Diketahui pada sebuah sekolah, seorang murid dapat mengambil banyak mata kuliah,
dan sebuah mata kuliah dapat diambil oleh beberapa murid.

Anda sebagai *programmer* yang bekerja pada sekolah tersebut, diminta untuk
membuat sebuah aplikasi untuk me-listing murid dan course yang dapat mereka
ambil, dengan persyaratan sebagai berikut:

## Langkah 1 - Buat Database
Dengan menggunakan sequelize, buatlah sebuah tabel dengan nama `dev`.

## Langkah 2 - Buat Tabel
Dengan diberikan struktur tabel seperti berikut, buatlah tabel dengan
menggunakan `sequelize`

`Courses`
| Field     | Type         | Description                |
|:----------|:-------------|:---------------------------|
| id        | INTEGER      | AUTO INCREMENT, PRIMARY KEY|
| name      | VARCHAR(255) | NOT NULL                   |
| max_caps  | INTEGER      | NOT NULL                   |
| createdAt | TIMESTAMP    | NOT NULL                   |
| updatedAt | TIMESTAMP    | NOT NULL                   |

`Students`
| Field     | Type        | Description                 |
|:----------|:------------|:----------------------------|
| id        | INTEGER     | AUTO INCREMENT, PRIMARY KEY |
| firstName | VARCHAR(255)| NOT NULL                    |
| lastName  | VARCHAR(255)| NOT NULL                    |

`Learning`
| Field     | Type        | Description                 |
|:----------|:------------|:----------------------------|
| id        | INTEGER     | AUTO INCREMENT, PRIMARY KEY |
| CourseId  | INTEGER     | FOREIGN KEY, NOT NULL       |
| StudentId | INTEGER     | FOREIGN KEY, NOT NULL       |

## Langkah 3 - Populasikan Data

Dengan diberikan data dalam bentuk `data/students.json` dan `data/courses.json`,
buatlah seeder pada `sequelize` untuk mempopulasikan data pada Tabel tertentu.

## Langkah 4 - Buat Routing

Dengan diberikan data endpoint sebagai berikut, buatlah routingnya !

| Endpoints         | Description                                    |
|:------------------|:-----------------------------------------------|
| GET /students     | Tampilkan seluruh murid dalam bentuk tabel     |
| GET /students/add | Tampilkan form untuk penambahan murid          |
| POST /students/add| handle form penambahan murid                   |
| GET /courses      | Tampilkan seluruh pelajaran dalam bentuk tabel |
| GET /courses/add  | Tampilkan form untuk penambahan pelajaran      |
| POST /courses/add | handle form penambahan pelajaran               | 
| GET /learning     | Tampilkan nama pembelajaran dan nama muridnya  |
| GET /learning/add | Tampilkan form penambahan pembelajaran         |
| POST /learning/add| hanlde form penambahan pembelajaran            |

## Langkah 5 - Implementasikan GET /students
Buatlah sebuah halaman dalam bentuk tabel untuk menampilkan data dari
murid yang ada pada Tabel `Students`

## Langkah 6 - Implementasikan GET /students/add
Buatlah sebuah halaman yang berisi sebuah form untuk menambahkan murid

## Langkah 7 - Implementasikan POST /students/add
Buatlah logic untuk menghandle form penambahan murid pada `GET /students/add`

## Langkah 8 - Implementasikan GET /courses
Buatlah sebuah halaman dalam bentuk tabel untuk menampilkan data dari
pelajaran yang ada pada tabel `Courses`

## Langkah 9 - Implementasikan GET /courses/add
Buatlah sebuah halaman yang berisi sebuah form untuk menambahan pelajaran

## Langkah 10 - Implementasikan POST /courses/add
Buatlah logic untuk menghandle form penambahan pelajaran pada `GET /courses/add`

## Langkah 11 - Implementasikan GET /learning
Buatlah sebuah halaman dalam bentuk tabel untuk menampilkan data dari
pembelajaran dalam bentuk `Learning` id, `Courses` name, 
dan `Students` firstName + `Students` lastName

## Langkah 12 - Implementasikan GET /learning/add
Buatlah sebuah halaman yang berisi sebuah form untuk menambahkan pembelajaran,
Halaman ini berisi Nama Pelajar dan Nama Pelajaran yang bisa dipilih melalui
`dropdown`.

## Langkah 13 - Implementasikan POST /learning/add
Buatlah logic untuk menghandle form dari `GET /learning/add`
