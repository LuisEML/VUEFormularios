 <script>
  export default{
    data: () => ({
      proyecto: "",
      tipo:"",
      urgente:false,
      proyectos: [],
    }),
    methods:{
      registrarProyecto(){
        const proyecto = {
          proyecto: this.proyecto,
          tipo: this.tipo,
          urgente: this.urgente,
        }
        this.proyectos.push(proyecto);

        this.proyecto = "";
        this.tipo = "";
        this.urgente = false;
      },
    },
  };

 </script>
 
 
 <template>
     <form @submit.prevent="registrarProyecto">
          <div class="mb-3">
            <label class="form-label">Proyecto</label>
            <input v-model="proyecto" type="text" class="form-control" required>
          </div>
          <div class="mb-3">
            <label class="form-label">Actividad</label>
            <select v-model.trim="tipo" class="form-select" required>
            <option value="" disabled selected>Selecciona un tipo de actividad</option>
            <option>Aplicaciones web con Vue.js</option>
            <option>Backend services con Node.js</option>
            <option>App móvil con React Native</option>
          </select>
          </div>
          <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">Urgente</label>
            <input v-model="urgente" type="checkbox" class="form-check-input">
          </div>
          <button type="submit" class="btn btn-primary">Submit</button>
        </form>
        <hr>
        <div class="table-responsive">
            <table class="table">
              <thead>
                <tr>
                  <th>#</th>
                  <th>Proyecto</th>
                  <th>Tipo</th>
                  <th>Urgente</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>1</td>
                  <td>{{proyecto}}</td>
                  <td>{{tipo}}</td>
                  <td class="bg-success">{{urgente}}</td>
                </tr>
              </tbody>
            </table>
        </div>
        
 </template>


 