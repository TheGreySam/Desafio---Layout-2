<template>
 <div>
  <b-navbar class="has-background-success">
        <template #brand >
            <b-navbar-item tag="router-link" :to="{ path: '/' }" class="is-size-2 has-text-white">
                Rick and Morty
            </b-navbar-item>
            
        </template>
        
    </b-navbar>
    <div class="columns">
      <div class="column is-flex " style="padding: 1%">
    <div 
    v-for="(personaje, $index) in personajes"
    :key="$index"
    class="card"
    style="width: 33%; padding: 1%">
  <div class="card-image">
    <figure class="image">
      <img :src="personaje.imagen" alt="Placeholder image"/>
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      
      <div class="media-content">
        <p class="title is-4">{{ personaje.nombre }}</p>
        
      </div>
    </div>
  </div>
</div>
</div>

    </div>
    
 </div>
    
    
</template>

<script>
export default {
    data: () => ({
        personajes: [
        {
        id: 1,
        nombre: 'Morty',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
        id: 2,
        nombre: 'Rick',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
        id: 3,
        nombre: 'Summer',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
        id: 4,
        nombre: 'Beth',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
        id: 5,
        nombre: 'Jerry',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        }
        ]
    }),

}    
</script>


