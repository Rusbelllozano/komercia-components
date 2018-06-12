<template>
<section class="container">
  <section class="settingBanner">
    <div  class="upload-area">
      <label for="uploadBanner" class="upload">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="cloud-up" role="presentation">
          <title  id="cloud-up" lang="en">cloud-up icon</title>
          <g fill="#FFF">
            <path  xmlns="http://www.w3.org/2000/svg" d="M17 6.75c0 2.343-1.906 4.25-4.25 4.25h-2.757v-1h2.757c1.792 0 3.25-1.458 3.25-3.25s-1.458-3.25-3.25-3.25c-0.532 0-1.057 0.141-1.56 0.417l-0.354 0.195-0.265-0.306c-0.719-0.829-1.748-1.306-2.821-1.306-1.661 0-3.099 1.080-3.576 2.688l-0.126 0.422-0.435-0.072c-0.119-0.019-0.238-0.038-0.363-0.038-1.24 0-2.25 1.009-2.25 2.25s1.010 2.25 2.25 2.25h3.699v1h-3.699c-1.792 0-3.25-1.458-3.25-3.25 0-1.826 1.529-3.335 3.353-3.248 0.713-1.812 2.431-3.002 4.397-3.002 1.234 0 2.42 0.494 3.309 1.367 0.546-0.244 1.113-0.367 1.691-0.367 2.344 0 4.25 1.907 4.25 4.25zM10.646 8.854l0.707-0.707-2.853-2.854-2.854 2.853 0.707 0.707 1.647-1.646v7.793h1v-7.793l1.646 1.647z">
            </path>
          </g>
        </svg>
        Subir imagenes
      </label>
      <input type="file" id="uploadBanner" @change="uploadPhoto($event, 0)" >
    </div>
  </section>

  <div class="input_area">
    <el-input placeholder="Titulo" v-model="setting[0].title">
      <template slot="prepend">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="text" role="presentation">
          <title  id="text" lang="en">text icon</title>
          <g  fill="currentColor">
            <path  d="M14 2v3h-1v-2h-4v12h1.643v1h-4.286v-1h1.643v-12h-4v2h-1v-3h11z" ></path>
          </g>
        </svg>
      </template>
    </el-input>

    <el-input placeholder="Descripcion" v-model="setting[0].description">
      <template slot="prepend">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="align-justify" role="presentation">
          <title id="align-justify" lang="en">align-justify icon</title>
          <g fill="currentColor">
            <path d="M17 2v1h-17v-1h17zM0 7h17v-1h-17v1zM0 11h17v-1h-17v1zM0 15h17v-1h-17v1z" fill="#000000" ></path>
          </g>
        </svg>
      </template>
    </el-input>

    <el-input placeholder="Url de redirección" v-model="setting[0].redirect_url">
      <template slot="prepend">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="links" role="presentation">
          <title id="links" lang="en">links icon</title>
          <g  fill="currentColor">
            <path  d="M12.983 6.94l-0.938 0.938-0.707-0.707 0.938-0.938c0.975-0.975 0.975-2.561 0-3.535s-2.561-0.975-3.535 0l-2.987 2.988c-0.975 0.975-0.975 2.561 0 3.535s2.561 0.975 3.535 0l0.707 0.707c-0.683 0.683-1.578 1.023-2.475 1.023s-1.792-0.341-2.474-1.023c-1.364-1.364-1.364-3.585 0-4.949l2.987-2.987c1.365-1.365 3.584-1.365 4.949 0 1.365 1.363 1.365 3.584 0 4.948zM6.042 8.034l-0.13 0.129 0.705 0.709 0.131-0.13c0.975-0.975 2.561-0.975 3.535 0s0.975 2.561 0 3.535l-3.023 3.025c-0.975 0.975-2.561 0.975-3.535 0s-0.975-2.561 0-3.535l1.058-1.059-0.707-0.707-1.058 1.059c-1.364 1.364-1.364 3.585 0 4.949 0.683 0.683 1.578 1.023 2.475 1.023s1.792-0.341 2.475-1.023l3.023-3.024c1.364-1.364 1.364-3.585 0-4.949-1.366-1.367-3.586-1.364-4.949-0.002z" fill="#000000" ></path>
          </g>
        </svg>
      </template>
    </el-input>

    <el-input placeholder="Texto del boton" v-model="setting[0].button_text">
      <template slot="prepend">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="text" role="presentation">
          <title  id="text" lang="en">text icon</title>
          <g  fill="currentColor">
            <path  d="M14 2v3h-1v-2h-4v12h1.643v1h-4.286v-1h1.643v-12h-4v2h-1v-3h11z" ></path>
          </g>
        </svg>
      </template>
    </el-input>
  </div>

  <section class="settingBanner">
    <div  class="upload-area">
      <label for="uploadBannerDown" class="upload">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="cloud-up" role="presentation">
          <title  id="cloud-up" lang="en">cloud-up icon</title>
          <g  fill="#FFF">
            <path  xmlns="http://www.w3.org/2000/svg" d="M17 6.75c0 2.343-1.906 4.25-4.25 4.25h-2.757v-1h2.757c1.792 0 3.25-1.458 3.25-3.25s-1.458-3.25-3.25-3.25c-0.532 0-1.057 0.141-1.56 0.417l-0.354 0.195-0.265-0.306c-0.719-0.829-1.748-1.306-2.821-1.306-1.661 0-3.099 1.080-3.576 2.688l-0.126 0.422-0.435-0.072c-0.119-0.019-0.238-0.038-0.363-0.038-1.24 0-2.25 1.009-2.25 2.25s1.010 2.25 2.25 2.25h3.699v1h-3.699c-1.792 0-3.25-1.458-3.25-3.25 0-1.826 1.529-3.335 3.353-3.248 0.713-1.812 2.431-3.002 4.397-3.002 1.234 0 2.42 0.494 3.309 1.367 0.546-0.244 1.113-0.367 1.691-0.367 2.344 0 4.25 1.907 4.25 4.25zM10.646 8.854l0.707-0.707-2.853-2.854-2.854 2.853 0.707 0.707 1.647-1.646v7.793h1v-7.793l1.646 1.647z">
            </path>
          </g>
        </svg>
        Subir imagenes
      </label>
        <input type="file" id="uploadBannerDown" @change="uploadPhoto($event, 1)" >
    </div>
  </section>
  <div class="input_area">
    <el-input placeholder="Titulo" v-model="setting[1].title">
      <template slot="prepend">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="text" role="presentation">
          <title  id="text" lang="en">text icon</title>
          <g  fill="currentColor">
            <path  d="M14 2v3h-1v-2h-4v12h1.643v1h-4.286v-1h1.643v-12h-4v2h-1v-3h11z" ></path>
          </g>
        </svg>
      </template>
    </el-input>

    <el-input placeholder="Descripcion" v-model="setting[1].description">
      <template slot="prepend">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="align-justify" role="presentation">
          <title id="align-justify" lang="en">align-justify icon</title>
          <g fill="currentColor">
            <path d="M17 2v1h-17v-1h17zM0 7h17v-1h-17v1zM0 11h17v-1h-17v1zM0 15h17v-1h-17v1z" fill="#000000" ></path>
          </g>
        </svg>
      </template>
    </el-input>

    <el-input placeholder="Url de redirección" v-model="setting[1].redirect_url">
      <template slot="prepend">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="links" role="presentation">
          <title  id="links" lang="en">links icon</title>
          <g  fill="currentColor">
            <path  d="M12.983 6.94l-0.938 0.938-0.707-0.707 0.938-0.938c0.975-0.975 0.975-2.561 0-3.535s-2.561-0.975-3.535 0l-2.987 2.988c-0.975 0.975-0.975 2.561 0 3.535s2.561 0.975 3.535 0l0.707 0.707c-0.683 0.683-1.578 1.023-2.475 1.023s-1.792-0.341-2.474-1.023c-1.364-1.364-1.364-3.585 0-4.949l2.987-2.987c1.365-1.365 3.584-1.365 4.949 0 1.365 1.363 1.365 3.584 0 4.948zM6.042 8.034l-0.13 0.129 0.705 0.709 0.131-0.13c0.975-0.975 2.561-0.975 3.535 0s0.975 2.561 0 3.535l-3.023 3.025c-0.975 0.975-2.561 0.975-3.535 0s-0.975-2.561 0-3.535l1.058-1.059-0.707-0.707-1.058 1.059c-1.364 1.364-1.364 3.585 0 4.949 0.683 0.683 1.578 1.023 2.475 1.023s1.792-0.341 2.475-1.023l3.023-3.024c1.364-1.364 1.364-3.585 0-4.949-1.366-1.367-3.586-1.364-4.949-0.002z" fill="#000000" ></path>
          </g>
        </svg>
      </template>
    </el-input>
    <el-input placeholder="Texto del boton" v-model="setting[1].button_text">
      <template slot="prepend">
        <svg  xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" aria-labelledby="text" role="presentation">
          <title  id="text" lang="en">text icon</title>
          <g  fill="currentColor">
            <path  d="M14 2v3h-1v-2h-4v12h1.643v1h-4.286v-1h1.643v-12h-4v2h-1v-3h11z" ></path>
          </g>
        </svg>
      </template>
    </el-input>
  </div>
</section>
</template>

<script>
import axios from 'axios';
export default {
  name: 'setting',
  props: ['setting'],
  data () {
   return {
        dialogImageUrl: '',
        dialogVisible: false
    }
  },
  methods: {
    uploadPhoto(event, position){
      console.log(position);
      let params=new FormData();
      params.append('file', event.target.files[0]);
      params.append('upload_preset','sqqjeaf4');
      axios.post('https://api.cloudinary.com/v1_1/maincra/image/upload', params)
      .then( (response) => {
        this.setting[position].photo = response.data.url;
      })
      .catch(function (error) {
    console.log(error);
      });
    }
  },
}
</script>

<style scoped>

.container{
 width: 20%;
 font-family: helvetica;
}

.input_area{
  display: flex;
  flex-direction: column;
  width: 300px;
  margin: 0;
}

.settingBanner{
  padding: 20px 0;
  border-bottom: 1px solid;
}

.upload-area{
  width: 100%;
  height: 100px;
  background-color:#f4f6f8;
  display: grid;
  justify-items: center;
  align-content: center;
}

.upload{
  background-color: #4834d4;
  cursor: pointer;
  padding: 10px;
  color: white;
  text-align: center;

}

#uploadBanner{
  display: none;
}

#uploadBannerDown{
  display: none;
}

.el-input {
    width: 250px;
    margin: 5px;
  }

</style>
