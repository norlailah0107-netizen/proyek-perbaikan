# proyek-perbaikan

## KODE PERBAIKAN
def cek_bilangan_genap(angka):
    if angka % 2 == 0:
        return True
    return False

## PENGUJIAN
from kode_perbaikan import cek_bilangan_genap

def jalankan_pengujian():
    assert cek_bilangan_genap(2) == True
    assert cek_bilangan_genap(4) == True
    assert cek_bilangan_genap(0) == True
    assert cek_bilangan_genap(3) == False
    assert cek_bilangan_genap(5) == False
    print("✅ SEMUA UJI BERHASIL!")

jalankan_pengujian()