# ==================================================
# ❌ KODE ASLI / BERMASALAH
# ==================================================
def cek_salah(angka):
    if angka % 2:          # 0 % 2 = 0 → dianggap salah
        return False
    return True

# ==================================================
# ✅ KODE SUDAH DIPERBAIKI
# ==================================================
def cek_genap(angka):
    if angka % 2 == 0:     # Cek sisa bagi = 0 secara jelas
        return True
    return False

# ==================================================
# 🧪 HASIL PENGUJIAN
# ==================================================
print("=" * 50)
print("PERBANDINGAN: KODE ASLI vs PERBAIKAN")
print("=" * 50)

print(f"❌ Kode asli — cek_salah(0) = {cek_salah(0)}  (salah, 0 itu genap)")
print(f"✅ Kode perbaikan — cek_genap(0) = {cek_genap(0)}  (benar)")

print("\n" + "=" * 50)
print("DETAIL UJI COBA")
print("=" * 50)

uji = [
    (0, True,  "genap"),
    (2, True,  "genap"),
    (4, True,  "genap"),
    (3, False, "ganjil"),
    (5, False, "ganjil"),
]

berhasil = True
for angka, hasil_harap, keterangan in uji:
    hasil_nyata = cek_genap(angka)
    status = "✅" if hasil_nyata == hasil_harap else "❌"
    if hasil_nyata != hasil_harap: berhasil = False
    print(f"{status} cek_genap({angka}) = {hasil_nyata} | seharusnya {hasil_harap} ({keterangan})")

print("=" * 50)
print("✅ SEMUA UJI BERHASIL!" if berhasil else "❌ ADA YANG SALAH!")
print("=" * 50)