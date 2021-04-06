<?php
            $names= ["romt", "mean", "xean", "vxer","raham"];
            function vokal($kalimat) {
            $a = substr_count($kalimat, 'a');
            $i = substr_count($kalimat, 'i');
            $u = substr_count($kalimat, 'u');
            $e = substr_count($kalimat, 'e');
            $o = substr_count($kalimat, 'o');

            $count = ($a+$i+$u+$e+$o);

            return $count;
          }

          function konsonan($kalimat) {
            $jumlah = strlen($kalimat);
            $a = substr_count($kalimat, 'a');
            $i = substr_count($kalimat, 'i');
            $u = substr_count($kalimat, 'u');
            $e = substr_count($kalimat, 'e');
            $o = substr_count($kalimat, 'o');

            $count = $jumlah - ($a+$i+$u+$e+$o);

            return $count;
        }


           <?php foreach ($names as $name) :  ?>

                    <?php
                         echo "<br>";
                         echo " Nama           :". $name."<br>"; 
                         echo " Jumlah Huruf   :". strlen($name)."<br>"; 
                         echo " Jumlah Kata    :". str_word_count($name)."<br>"; 
                         echo " Kebalikan Nama :". strrev($name)."<br>"; 
                         echo " Huruf Vokal    :". vokal(  $name)."<br>";  
                         echo " Huruf Konsonan :". konsonan( $name)."<br>"; 
                         echo "<br>"; 
                    ?>
                      <?php endforeach; ?>


</body>
</html>

