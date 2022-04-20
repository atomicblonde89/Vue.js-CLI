<template>
    <div id="app" class="container">
        <h1 class="text-center">Tabla de Usuarios</h1>
        <table class="table table-bordered table-hover table-striped">
            <thead>
                <tr>
                    <th>#</th>
                    <th>Nombre</th>
                    <th>Apellido</th>
                    <th>Run</th>
                    <th>Fecha Nacimiento</th>
                    <th>Edad</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(usuario,i) in usuarios" :key="i">
                    <th>{{i+1}}</th>
                    <td>{{usuario.nombre}}</td>
                    <td>{{usuario.apellido}}</td>
                    <td>{{usuario.run}}</td>
                    <td>{{usuario.nacimiento}}</td>
                    <td>{{usuario.edad}}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>

export default {
 name: "App",
 data: () => {
               let result = { usuarios: [
                    {
                        nombre: 'Jose',
                        apellido: 'Pérez',
                        run: '123456-2',
                        nacimiento: '12-04-67',
                        edad: 52,},
                    {
                        nombre: 'María',
                        apellido: 'Rodríguez',
                        run: '654321-1',
                        nacimiento: '30-11-90',
                        edad: 29,},
                    
                    {   nombre: 'Manuel',
                        apellido: 'Patiño',
                        run: '142223456-6',
                        nacimiento: '02-12-59',
                        edad: 60,},
                ]
            }
            return result
        }
        }
        
        
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
