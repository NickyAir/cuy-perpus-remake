---
config:
  theme: redux-dark
  layout: elk
---
classDiagram
  class User {
    Int id
    String username
    String email
    String password
    Role role
    DateTime createdAt
  }

  class Book {
    Int id
    String judul
    String penulis
    String penerbit
    String thumbnail
    Int tahunTerbit
  }

  class Kategori {
    Int id
    String nama
  }

  class Peminjaman {
    Int id
    DateTime tanggalPinjam
    DateTime? tanggalKembali
    Status status
  }

  class Role {
    <<enum>>
    ADMIN
    PETUGAS
    USER
  }

  class Status {
    <<enum>>
    DIPINJAM
    DIKEMBALIKAN
  }

  User "1" --> "many" Peminjaman : meminjam
  Book "1" --> "many" Peminjaman : dipinjam dalam
  Peminjaman "many" --> "1" User : milik user
  Peminjaman "many" --> "1" Book : terkait buku

  Kategori "1" --> "many" Book : dimiliki oleh
  Book "many" --> "1" Kategori : masuk ke
