# Buat Apa ini?

Repo ini merupakan sumber daftar lembaga pemerintah. Data ini untuk sementara digunakan untuk aplikasi perpajakan daerah. Sehingga datanya tidak begitu lengkap

> Data untuk sementara difokuskan untuk Kabupaten Garut

# Sumber

Data bersumber dari aturan-aturan pemerintah yang resmi. Berikut Daftarnya

| Aturan | tentang | Link |
| --------- | ------ | ----- |
| PPeraturan Bupati (PERBUP) Kabupaten Garut Nomor 194 Tahun 2023 tentang Perubahan Keenam Atas Peraturan Bupati Nomor 27 Tahun 2016 Tentang Kedudukan dan Susunan Organisasi Perangkat Daerah Kabupaten Garut | Daftar Lembaga Pemda Garut | [Link](https://peraturan.bpk.go.id/Details/284968/perbup-kab-garut-no-194-tahun-2023) |

# Contoh Penarikan

```typescript
// Nextjs 14 typescript
const fetchData = async () => {
  try {
    const response = await fetch(
      `https://raw.githubusercontent.com/rafadlislembaga-pemerintah/main/data.json`
    );
    if (response.ok) {
      const { data } = await response.json();
      setLembagaGarut(data);
    }
  } catch (error) {
    console.log("Error fetching data:", error);
  }
};
fetchData()
```
