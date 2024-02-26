# Desain-OOP
Berikut adalah desain OOP untuk aplikasi manajemen data karyawan dengan PHP:
```
1. Kelas Employee:
   A. Atribut:
      id: ID karyawan
      name: Nama karyawan
      position: Posisi karyawan
      salary: Gaji karyawan
   B. Metode:
      __construct($id, $name, $position, $salary): Konstruktor untuk inisialisasi atribut
      getId(): Mengembalikan ID karyawan
      getName(): Mengembalikan nama karyawan
      getPosition(): Mengembalikan posisi karyawan
      getSalary(): Mengembalikan gaji karyawan
      updateSalary($newSalary): Memperbarui gaji karyawan

2. Kelas EmployeeManagement:
   A. Atribut:
      employees: Array untuk menyimpan objek karyawan
   B. Metode:
      addEmployee($employee): Menambahkan karyawan baru ke dalam daftar
      removeEmployee($employee): Menghapus karyawan dari daftar
      findEmployeeById($id): Mencari karyawan berdasarkan ID
      calculatePayroll(): Menghitung total gaji seluruh karyawan
      generatePayrollReport(): Mencetak slip gaji untuk setiap karyawan
3. Hubungan antar kelas:
   Employee dan EmployeeManagement memiliki hubungan agregasi. EmployeeManagement memiliki koleksi objek Employee.
4. Contoh kode PHP untuk menambahkan karyawan baru:

    <?php
    
    class Employee {
        private $id;
        private $name;
        private $position;
        private $salary;
    
        public function __construct($id, $name, $position, $salary) {
            $this->id = $id;
            $this->name = $name;
            $this->position = $position;
            $this->salary = $salary;
        }
    
        public function getId() {
            return $this->id;
        }
    
        public function getName() {
            return $this->name;
        }
    
        public function getPosition() {
            return $this->position;
        }
    
        public function getSalary() {
            return $this->salary;
        }
    
        public function updateSalary($newSalary) {
            $this->salary = $newSalary;
        }
    }
    
    class EmployeeManagement {
        private $employees = [];
    
        public function addEmployee($employee) {
            $this->employees[] = $employee;
        }
    
        public function getEmployees() {
            return $this->employees;
        }
    }
5. Diagram UMLnya: <img src="https://firebasestorage.googleapis.com/v0/b/cart-c80d1.appspot.com/o/Cuplikan%20layar%202024-02-26%20092948.jpg?alt=media&token=20d599e7-0e3c-46ab-a679-0e04c08a937f"/>
```
