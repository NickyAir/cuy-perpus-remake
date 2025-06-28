## CuyPerpus

CuyPerpus adalah project perpustakaan digital yang sebelumnya dibuat menggunakan native PHP, namun belum selesai. Project ini sedang dikembangkan ulang dengan struktur dan fitur yang sama, namun menggunakan teknologi modern seperti Next.js, Docker, dan Prisma.

## Cara jalankan dan review projek ini?

- Pastikan sudah mempunyai **Docker** lalu jalankan perintah berikut ini jika pertama kali ingin menjalankan Project **CuyPerpus**

```bash
docker compose up --build
```

## Cara mengembangkan project ini?

- Backend Developer:
  Salin file `.env.example` menjadi `.env` dan sesuaikan konfigurasi database jika diperlukan.

  > Kami menyarankan menggunakan `Laragon` jika kamu belum menginstall `Docker` secara local

  Lakukan pengembangan pada folder:
  `src/app/api/` -> API Routes (Controllers)
  `prisma/schema.prisma` -> Skema dan migrasi database

  Jalankan perintah berikut :

  ```bash
  npx prisma generate # Generate Prisma Client WAJIB
  npx prisma migrate dev # (Opsional) Jalankan migrasi database jika belum ada database
  npx prisma db seed # (Opsional) Seeding database dengan data dummy yang sudah ditentukan
  ```

> Pastikan Databse sudah menyala sebelum menjalankan perintah Prisma

  <br>

- Frontend Developer:
  Install Dependencies terlebih dahulu:

```bash
npm i
#Atau jika kamu menggunakan PNPM
pnpm i
```

Kembangkan UI dan UX pada folder:
`src/app/`

- [Endpoint Dokumentasi](https://github.com/ade-nugraha306/cuy-perpus-remake/blob/master/README.md)

**PENTING!!**

- Frontend Developer dilarang mengubah isi folder `src/app/api/` karena itu merupakan domain kerja Backend Developer.

- Backend Developer dilarang mengubah isi folder `src/app/` karena itu merupakan domain kerja Frontend Developer.

## Say Hi kepada para kontribusi kami!

- [Ade Nugraha](https://github.com/ade-nugraha306)
- [Gusty Erlana Aldiansyah](https://github.com/crytomzrt)
- [Fahlevy Miasya Rangkuti](https://github.com/Rangkuti-Code)

---

## CuyPerpus

CuyPerpus is a digital library project that was originally built using native PHP, but left unfinished. This remake project aims to rebuild it using the same structure and features—but powered by modern technologies like **Next.js**, **Docker**, and **Prisma**.

## How to Run and Review this Project

Make sure **Docker** is installed on your machine, then run the following command to build and start the app for the first time:

```bash
docker compose up --build
```

## How to Develop This Project

- Backend Developer
  Copy `.env.example` to `.env` and adjust the database configuration if needed.
  > We recommend using Laragon if you're not using Docker locally.

Work inside the following folders:
`src/app/api/` → API Routes (Controllers)
`prisma/schema.prisma` → Database schema and migrations

Run These Commands:

```bash
  npx prisma generate # Generate Prisma Client
  npx prisma migrate dev # (Optional) Run database migrations if there are no databases on your local machine
  npx prisma db seed # (Optional) Run database seeding with dummy data
```

> Make sure the database is up and running before running any Prisma commands.

- Frontend Developer
  Install Dependencies:

```bash
npm i
#Or if you're using PNPM
pnpm i
```

Work on UI/UX development inside the folder:
`src/app/`

- [Endpoint Documentations](https://github.com/ade-nugraha306/cuy-perpus-remake/blob/master/README.md)

**IMPORTANT!!**

- **Frontend Developers** must not edit or access `src/app/api/`, as it is exclusively for backend development.

- **Backend Developers** must not edit or access `src/app/`, as it is exclusively for frontend development.

## Say Hi to our contributors

- [Ade Nugraha](https://github.com/ade-nugraha306)
- [Gusty Erlana Aldiansyah](https://github.com/crytomzrt)
- [Fahlevy Miasya Rangkuti](https://github.com/Rangkuti-Code)
