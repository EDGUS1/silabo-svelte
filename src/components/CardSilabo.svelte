<script>
  let isFavorito = true;

  const toggleFavourite = () => (isFavorito = !isFavorito);
</script>

<div class="card border-secondary mb-3">
  <div class="card-body">
    <span class="card-title d-flex justify-content-between align-items-center">
      <span class="h5">Nombre curso</span>
      <button
        class="btn {isFavorito ? 'btn-danger' : 'btn-outline-danger'}"
        on:click={toggleFavourite}
        >H
        <!-- <fa-icon [icon]="faHeart"></fa-icon> -->
      </button>
    </span>
    <hr />
    <p>
      <small>Ciclo: </small> -
      <small>Periodo: </small>
    </p>
    <p class="card-text">Sumilla</p>
    <div class="d-flex justify-content-between align-items-center row">
      <div class="col-md-7">
        <button class="btn btn-info">
          P<!-- <fa-icon [icon]="faPen"></fa-icon> -->
        </button>
        <button class="btn btn-warning mx-1"
          >T
          <!-- <fa-icon [icon]="faTrashAlt"></fa-icon> -->
        </button>
        <button class="btn btn-primary"
          >D
          <!-- <fa-icon [icon]="faFileDownload"></fa-icon> -->
        </button>
      </div>
      <div class="col-md-5 mt-3 mt-md-0 p-0">
        <small>Fecha actualización</small>
      </div>
    </div>
  </div>
</div>
