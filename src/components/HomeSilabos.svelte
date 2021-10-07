<script>
  import CardSilabo from './CardSilabo.svelte';

  let isLista = false;
  const cambiarLista = () => (isLista = true);

  const cambiarGrid = () => (isLista = false);
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
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                fill="currentColor"
                class="bi bi-list-ul"
                viewBox="0 0 16 16"
              >
                <path
                  fill-rule="evenodd"
                  d="M5 11.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm-3 1a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm0 4a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm0 4a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"
                />
              </svg>
            </button>
            <button
              type="button"
              class="btn {isLista ? 'btn-outline-secondary' : 'btn-secondary'}"
              on:click={cambiarGrid}
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                fill="currentColor"
                class="bi bi-grid-3x3-gap"
                viewBox="0 0 16 16"
              >
                <path
                  d="M4 2v2H2V2h2zm1 12v-2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1zm0-5V7a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1zm0-5V2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1zm5 10v-2a1 1 0 0 0-1-1H7a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1zm0-5V7a1 1 0 0 0-1-1H7a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1zm0-5V2a1 1 0 0 0-1-1H7a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1zM9 2v2H7V2h2zm5 0v2h-2V2h2zM4 7v2H2V7h2zm5 0v2H7V7h2zm5 0h-2v2h2V7zM4 12v2H2v-2h2zm5 0v2H7v-2h2zm5 0v2h-2v-2h2zM12 1a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1h-2zm-1 6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V7zm1 4a1 1 0 0 0-1 1v2a1 1 0 0 0 1 1h2a1 1 0 0 0 1-1v-2a1 1 0 0 0-1-1h-2z"
                />
              </svg>
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
