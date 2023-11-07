## **TUGAS PEMROGRAMAN ORIENTASI OBJEK**

Nama : Aditia Seftiawan  
Nim  : 312210094  
Kelas : TI.22.B1  
Matakuliah : Pemrograman Orientasi Objek  

## Source code 
``` Java
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace tugas6
{
    public class Pegawai
    {
        private string _nama;
        private double _gajiPokok;

        public void setNama(string paramNama)
        {
            _nama = paramNama;
        }
        // Aditia Seftiawan (312210094)
        public string getNama()
        {
            return _nama;
        }
        public void setGajiPokok(double paramGaji)
        {
            _gajiPokok = paramGaji;
        }

        public double getGajiPokok()
        {
            return _gajiPokok;
        }

        public virtual void cetakInfo()
        {
            Console.WriteLine("Pegawai : " + getNama());
            Console.WriteLine("Gaji Pokok : " + getGajiPokok());
        }
    }
    public class Manager : Pegawai
    {
        private double _tunjangan;

        public void setTunjangan(double paramTunjangan)
        {
            _tunjangan = paramTunjangan;
        }
        public double getTunjangan()
        {
            return _tunjangan;
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + getTunjangan());
        }
        public virtual void cetakInfo()
        {
            Console.WriteLine("Pegawai : " + getNama());
            Console.WriteLine("Posisi anda : Manager ");
            Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
        }
    }
    // Aditia Seftiawan (312210094)

    public class Programmer : Pegawai
    {
        private double _bonus;

        public void setBonus(double paramBonus)
        {
            _bonus = paramBonus;
        }

        public double getBonus()
        {
            return _bonus;
        }

        public void cetakBonus()
        {
            Console.WriteLine("Bonus Anda : " + getBonus());
        }

        public virtual void cetakInfo()
        {
            Console.WriteLine("Pegawai : " + getNama());
            Console.WriteLine("Posisi : Programer");
            Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
        }
    }
    // Aditia Seftiawan (312210094)

    class program{
        static void Main(string[] args)
        {
            Console.WriteLine("==========Pegawai Class==========");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Sofyan Pegawai");
            pegawai.setGajiPokok(19000000);
            pegawai.cetakInfo();

            Console.WriteLine("==========Manager Class==========");
            Manager manager = new Manager();
            manager.setNama("Adit Manager");
            manager.setGajiPokok(47000000);
            manager.setTunjangan(10000000);
            manager.cetakInfo();
            manager.cetakTunjangan();

            Console.WriteLine("==========Programer Class==========");
            Programmer programer = new Programmer();
            programer.setNama("Orta Programer");
            programer.setGajiPokok(30000000);
            programer.setBonus(5000000);
            programer.cetakInfo();
            programer.cetakBonus();
        }
    }
}
```

## Hasil
<img width="960" alt="image" src="https://github.com/aditia0110/Tugas6OOP/assets/115475348/a22778a3-7fc9-43e8-b105-c46105f79e97">
