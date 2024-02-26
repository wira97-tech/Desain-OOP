# Desain-OOP
Berikut adalah desain OOP untuk aplikasi manajemen data karyawan dengan PHP:

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
5. Diagram UMLnya:
<script type="text/javascript">window.vpov="16.3"</script><script type="text/javascript">window.vpob="20220410"</script><div class="mxgraph" style="max-width:100%;border:1px solid transparent;" data-mxgraph="{&quot;highlight&quot;:&quot;#0000ff&quot;,&quot;mKd&quot;:true,&quot;resize&quot;:true,&quot;page&quot;:0,&quot;toolbar&quot;:&quot;pages zoom layers lightbox&quot;,&quot;edit&quot;:&quot;https://online.visual-paradigm.com/app/diagrams/#diagram:proj=0&amp;type=ClassDiagram&amp;width=11&amp;height=8.5&amp;unit=inch&quot;,&quot;editBlankUrl&quot;:&quot;https://online.visual-paradigm.com/app/diagrams/#diagram:proj=0&amp;vpov=16.3&amp;vpob=20220410&amp;client=1&amp;edit=_blank&quot;,&quot;xml&quot;:&quot;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&quot;}"></div>
<script type="text/javascript" src="https://cdn-latest.visual-paradigm.com/diagrams/js/viewer.launcher.js"></script>
