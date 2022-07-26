###### Nama : aditya sixtiawan
###### kelas : RPL
###### No. Absen : 07

# Modul 1

soal nomor 1
Lakukan proses instalasi framework laravel kedalam folder dengan nama masing-masing

```
composer create-project laravel/laravel penjualan
```


# modul 2
soal nomor 1
Buatlah migration tabel kategori dengan menggunakan teknik yang telah di pelajari dalam modul ini.

langkah pertama
```
php artisan make:migration create_produk_table>
```

langkah kedua
isikan kode dibawah ini kedalam file yang dibuat
```
<?php

use Illuminate\Database\Migration\Migration;
use Illuminate\Database\Schema\Bluprint;
use Illuminate\Support\Facades\Schema;

return new class extends Migration
{
    /**
     * Run the migrations.
     *
     * @return void
     */
    public function up()
    {
        Schema::create('produk', function (Blueprint $table) {
            $table->id();
            $table->('nama');
            $table->timestamps();
        });
    }

    /**
     * Reverse the migrations.
     *
     * @return void
     */
    public function down()
    {
        Schema::dropIfExists('produk');
    }
};

### Langkah kedua
php artisan migrate


Soal No.2
Berikan data menggunakan seeder yang telah anda pelajari pada modul ini

<?php

namespace Database\Seeder:

useIIIuminate\Database\Console\Seeds\WithoutModelEvents;
useIIIuminate\Database\Seeder;
useDB;
class kategoritableseeder extends Seeder
{
    /**
    * Run the Database seeds.
    *
    @return void
    */
    public function run()
    {
       DB:table('kategori')->insert(array(
            [ 
                 'nama'=>'perlengkapan sekolah',
            ],
            [
                 'nama'=>'komputer',
            ],
            [
                 'nama'=>'Sabun',
            ],
            [
                 'nama'=>'ATK',
            ],
        ));
     )
)
```
