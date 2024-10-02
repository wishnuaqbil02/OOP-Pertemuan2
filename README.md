# OOP-Pertemuan2

# Input Code :
## Data Pesawat
```java
public class PesawatTempur {

    private final String warna;
    private int ketinggian; 
    private int kecepatan; 
    private int energi; 
    private String arah;
    private static final int MAX_KECEPATAN = 900;
    private static final int MAX_KETINGGIAN = 10000; 

    public PesawatTempur(String warna) {
        this.warna = warna;
        this.ketinggian = 0;
        this.kecepatan = 0;
        this.energi = 100;
        this.arah = "Utara";
    }
```
## Fungsi Menyalakan Pesawat
```java
public void nyalakanMesin() {
        System.out.println("Mesin pesawat dinyalakan...");
    }
```
## Fungsi Terbang
```java
public void terbang() {
        if (this.kecepatan > 0) {
            if (this.energi >= 10) { 
                this.energi -= 10; // 
                System.out.println("Pesawat terbang...");
            } else {
                System.out.println("Energi tidak cukup untuk terbang.");
            }
        } else {
            System.out.println("Pesawat harus memiliki kecepatan untuk terbang.");
        }
    }
```
## Fungsi Tambah Kecepatan
```java
public void tambahKecepatan(int kecepatan) {
        this.kecepatan += kecepatan;
        if (this.kecepatan > MAX_KECEPATAN) {
            this.kecepatan = MAX_KECEPATAN; 
        }
        System.out.println("Kecepatan pesawat bertambah menjadi " + this.kecepatan + " km/jam");
    }
```
## Fungsi Kurangi Kecepatan
```java
public void kurangiKecepatan(int kecepatan) {
        this.kecepatan -= kecepatan;
        if (this.kecepatan < 0) {
            this.kecepatan = 0; 
        }
        System.out.println("Kecepatan pesawat berkurang menjadi " + this.kecepatan + " km/jam");
    }
```
## Fungsi Belok
```java
public void belok(String arah) {
        this.arah = arah;
        System.out.println("Pesawat berbelok ke arah " + this.arah);
    }
```
## Funsgi Turun
```java
public void turun() {
        if (this.ketinggian - 100 >= 0) {
            this.ketinggian -= 100;
            System.out.println("Pesawat turun ke ketinggian " + this.ketinggian + " meter");
        } else {
            System.out.println("Pesawat sudah berada di ketinggian minimum.");
        }
    }
```
## Menampilkan Informasi Pesawat
```java
public void infoPesawat() {
        System.out.println("------------------------");
        System.out.println("Informasi Pesawat:");
        System.out.println("Warna: " + this.warna);
        System.out.println("Ketinggian: " + this.ketinggian + " meter");
        System.out.println("Kecepatan: " + this.kecepatan + " km/jam");
        System.out.println("Energi: " + this.energi + "%");
        System.out.println("Arah: " + this.arah);
        System.out.println("------------------------");
    }
```
## Membuat Objek Pesawat
```java
public static void main(String[] args) {

        PesawatTempur pesawat = new PesawatTempur("Merah");
```
## Menapilkan Informasi Awal Pesawat
```java
        pesawat.infoPesawat();
```
## Menyalakan Mesin Pesawat
```java
        pesawat.nyalakanMesin();
```
## Menambah Kecepatan Pesawat
```java
        pesawat.tambahKecepatan(200);
```
## Mengurangi Kecepatan Pesawat
```java
        pesawat.kurangiKecepatan(100);
```
## Mengubah Arah ke Barat
```java
        pesawat.belok("Barat");
```
## Turun 
```java
        pesawat.turun();
```
## Menapilkan Kembali Informasi Pesawat
```java
        pesawat.infoPesawat();
```
# Output :
![](OOP-Pertemuan2/output.png)
