## **TUGAS PEMROGRAMAN ORIENTASI OBJEK**

Nama : Garnish andhika Pratama  
Nim  : 312210161  
Kelas : TI.22.B1  
Matakuliah : Pemrograman Orientasi Objek  

## Source code 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace oop67
{
     public class Pegawai
    {
        

        private string nama;
        private double gajiPokok;

        public void setNama(string nama)
        {
            this.nama = nama;
        }
        public string getNama() { return this.nama; }

        public double getGajiPokok() { return this.gajiPokok; }

        public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

        public void cetakinfo()
        {

            Console.WriteLine("Nama : " + this.nama);
            Console.WriteLine("Gapok : " + this.gajiPokok);
        }
    }


    public class manager : Pegawai
    {
           
        private double tunjangan;

        public void setTunjangan(double tunjangan){this.tunjangan = tunjangan;}
        public double getTunjangan(){return this.tunjangan;}

        public new void cetakinfo()
        {
            
            base.cetakinfo();
            this.cetakTunjangan();
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + this.tunjangan);
            
        }
    }

    public class Programmer : Pegawai
    {
        private double bonus;


        public void setBonus(double bonus) { this.bonus = bonus; }

        public double getBonus() { return this.bonus; }

        public new void cetakinfo()
        {
            base.cetakinfo();
            this.cetakBonus();
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus : " + this.bonus);
            
            
        }
        
    }
    class program
    {
        static void Main(string[] args) 
        {
            Console.WriteLine("==== PEGAWAI ====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Garnish ");
            pegawai.setGajiPokok(300000);
            pegawai.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== MANAGER ====");
            manager Manager = new manager();
            Manager.setNama("Garnish");
            Manager.setGajiPokok(300000);
            Manager.setTunjangan(500000);
            Manager.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== PROGRAMMER ====");
            Programmer programer = new Programmer();
            programer.setNama("Garnish");
            programer.setGajiPokok(300000);
            programer.setBonus(10000000);
            programer.cetakinfo();
            Console.WriteLine();


            Console.WriteLine("press anykey");
            Console.ReadKey();
        }
    }
}

## Hasil
![image](https://github.com/Garnish16/TUGASoop6-7/assets/115474050/c81b5455-cff4-4973-adf2-31cc70c9435b)

