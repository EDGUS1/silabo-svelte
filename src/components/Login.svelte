<script>
</script>

<div class="card form-signin text-center mt-4">
  <form>
    <img
      class="my-4"
      src="/user.png"
      alt=""
      width="100"
      height="100"
    />
    <h1 class="h3 mb-3 fw-normal my-3">Inicio de sesión</h1>

    <div class="form-floating my-3">
      <input
        type="email"
        class="form-control"
        id="floatingInput"
        placeholder="name@example.com"
      />
      <label for="floatingInput">Correo institucional</label>
      <!-- <small class="text-danger mt-3 mt-lg-0"> Ingrese un correo válido </small> -->
    </div>
    <div class="form-floating my-3">
      <input
        type="password"
        class="form-control"
        id="floatingPassword"
        placeholder="Password"
      />
      <label for="floatingPassword">Contraseña</label>
      <!-- <small class="text-danger mt-3 mt-lg-0">
        Ingrese una contraseña válida
      </small> -->
    </div>

    <button class="w-100 btn btn-lg btn-primary" type="submit">
      Iniciar sesión
    </button>
    <p class="mt-5 mb-3 text-muted">&copy; 2021</p>
  </form>
</div>

<style>

  .form-signin {
    width: 100%;
    max-width: 330px;
    padding: 15px;
    margin: auto;
  }

  .form-signin .form-floating:focus-within {
    z-index: 2;
  }

  .form-signin input[type='email'] {
    margin-bottom: -1px;
    border-bottom-right-radius: 0;
    border-bottom-left-radius: 0;
  }

  .form-signin input[type='password'] {
    margin-bottom: 10px;
    border-top-left-radius: 0;
    border-top-right-radius: 0;
  }
</style>
