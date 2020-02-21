<?php
     $Mx = $_POST['Mx'] ; $My = $_POST['My'] ;
     $Nx = $_POST['Nx'] ; $Ny = $_POST['Ny'] ;
    $distance = sqrt(($Mx - $Nx)**2 + ($My - $Ny)**2)  ;
     
?>
<!DOCTYPE html>
<html lang="ru">
<body>
<div class="container text-center p-4">
    <?php if($distance): ?>
    <div class="alert alert-success">
        <?= "расстояние между точками: ${distance}" ?>
    </div>
    <?php endif ?>
    <form  method="POST"  enctype="multipart/form-data">
        <div class="form-group">
            <label>Первая точка</label>
            <input type="number" name="Mx" class="mx-2"  placeholder="Ввеите x">
            <input type="number" name="My" class="mx-2"  placeholder="Ввеите y">
        </div>
        <div class="form-group">
            <label>Вторая точка</label>
            <input type="number" name="Nx" class="mx-2" placeholder="Ввеите x">
            <input type="number" name="Ny" class="mx-2"  placeholder="Ввеите y">
        </div>
        <input type="submit" value="Отправить" class="btn btn-outline-primary" >
    </form>
</div>  
</body>
</html>
