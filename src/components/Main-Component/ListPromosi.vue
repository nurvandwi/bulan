<template>
  <div class="mb-3">
    <h3 class="font16 font-weight-bold mt-4 mb-0 ml-4">Data Kegiatan</h3>
    <p class="font-12 ml-4">Lengkapi data dibawah ini.</p>
    <div class="col-12">
      <router-link :to="{ path: 'registrasi' }">
        <div
          class="col shadow1 br text-left d-flex flex-row align-items-center my-3 py-4 px-3"
        >
          <img class="imagecustom pr-3" src="../../assets/icon-ktp.png" alt />

          <div class="align-items-center">
            <h5
              class="font14 formh2 caption4 p-0 m-0 text-dark font-weight-bold"
            >
              Data E-KTP & Data Bank
            </h5>
          </div>
          <img
            class="iconcustom ml-auto"
            src="https://i.imgur.com/5qg2kk5.png"
            alt
          />
        </div>
      </router-link>
    </div>
    <div class="col-12">
      <router-link :to="{ path: 'posm' }">
        <div
          class="col shadow1 text-left br d-flex flex-row align-items-center my-3 py-4 px-3"
        >
          <img class="imagecustom pr-3" src="../../assets/icon-posm.png" alt />

          <div class="align-items-center">
            <h5 class="font14 caption4 p-0 m-0 text-dark font-weight-bold">
              Upload Foto POSM & INVOICE
            </h5>
          </div>
          <img
            class="iconcustom ml-auto"
            src="https://i.imgur.com/5qg2kk5.png"
            alt
          />
        </div>
      </router-link>
    </div>
  </div>
</template>
<script>
/* eslint-disable */

export default {};
</script>
<style scoped>
.imagecustom {
  background-size: cover;
  height: 46px;
}

.shadow1 {
  box-shadow: 0 0.1rem 0.3rem rgba(182, 189, 255, 0.308) !important;
}

.br {
  border-radius: 15px;
}

.iconcustom {
  background-size: cover;
  height: 15px;
}

@media screen and (max-width: 1000px) {
  .font16 {
    font-size: 16px;
  }

  .font14 {
    font-size: 14px;
  }
  .font-12 {
    font-size: 12px;
  }
}
</style>
