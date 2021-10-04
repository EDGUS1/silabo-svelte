<script>
  import CardSilabo from './CardSilabo.svelte';

  let isLista = false;
  const cambiarLista = () => {
    isLista = true;
  };

  const cambiarGrid = () => {
    isLista = false;
  };
</script>

<div class="container">
  <div class="row my-4">
    <div class="col-12 col-lg-8">
      <div class="row">
        <div class="col-12 col-sm-4">
          <select class="form-select form-select-sm">
            <option value="0" hidden>Seleccione</option>
            <option value="1">Ordenar por nombre</option>
            <option value="2">Ordenar por fecha</option>
            <option value="3">Ordenar por favoritos</option>
          </select>
        </div>
        <div class="col-12 col-sm-8 mt-3 mt-sm-0">
          <input
            type="text"
            class="form-control form-control-sm"
            placeholder="Ingrese el nombre del curso del silabo"
          />
        </div>
      </div>
    </div>
    <div class="col-12 col-sm-8 col-lg-4 mt-3 mt-lg-0">
      <div class="row">
        <div class="col-4">
          <select class="form-select form-select-sm">
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="15">15</option>
          </select>
        </div>
        <div class="col-4">
          <div
            class="btn-group btn-group-md w-100"
            role="group"
            aria-label="Basic example"
          >
            <button
              type="button"
              class="btn {isLista ? 'btn-secondary' : 'btn-outline-secondary'}"
              on:click={cambiarLista}
            >
              <!-- <fa-icon [icon]="faList"></fa-icon> -->
              L
            </button>
            <button
              type="button"
              class="btn {isLista ? 'btn-outline-secondary' : 'btn-secondary'}"
              on:click={cambiarGrid}
              >G
              <!-- <fa-icon [icon]="faGrid"></fa-icon> -->
            </button>
          </div>
        </div>
        <div class="col-4 d-flex flex-row-reverse">
          <button type="button" class="btn btn-success px-4"> Crear </button>
        </div>
      </div>
    </div>
  </div>
  <div class="row my-3">
    <div class="col-12 col-md-6 col-lg-4">
      <CardSilabo />
    </div>
    <div class="col-12 col-md-6 col-lg-4">
      <CardSilabo />
    </div>
    <div class="col-12 col-md-6 col-lg-4">
      <CardSilabo />
    </div>

    <!-- <div #silaboslist>
        <div
          class="col-12"
          *ngFor="
            let silabo of silabos
              | search: 'asig_nombre':filterSearch
              | slice: (page - 1) * pageSize:page * pageSize
          "
        >
          <app-card-silabos-list [silabo]="silabo"></app-card-silabos-list>
        </div>
      </div> -->
    <!-- <div class="d-flex justify-content-center my-4">
      <ngb-pagination
          [(page)]="page"
          [pageSize]="pageSize"
          [collectionSize]="
            (silabos | search: 'asig_nombre':filterSearch)?.length
          "
        ></ngb-pagination>
    </div> -->
  </div>
  <!-- <ng-template #nosilabos>
      <div class="row my-5">
        <span class="h2">No tiene silabos creados</span>
      </div>
    </ng-template> -->
</div>
