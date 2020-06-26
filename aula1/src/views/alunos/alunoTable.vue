<template>
    <div>
    <table>
    <tr>
        <td>Nome</td>
        <td>Email</td>
        <td>Cidade</td>
        <td>Ações</td>
    </tr>
     <tr>
        <tr v=for="person in persons" : key="person.id">
            <td>{{ person.name}} </td>
             <td>{{ person.email}} </td>
              <td>{{ person.cidade}} </td>
        <td>
        <button class="btn btn-primary"> {{ btnAdd}} </button>
        <button class="btn btn-danger"> {{btnRemove}} </button>
        </td>
         
    </tr>
    </table>
    </div>
    </template>

    <script>

    export default{
        name: 'AlunoTemplate',
        data(){
            return{
        btnRemove:'Remover',
        btnAdd: 'Adicionar',
        persons: [{
            id: 001,
            name: 'Matheus',
            cidade: 'SP',
            email: 'xpto@terra.com.br',
        },
        {
            id: 002,
            name: 'Alexandre',
            cidade: 'SP',
            email: 'xpto@terra.com.br',

        },
        {
            id: 003,
            name: 'William',
            cidade: 'SC',
              email: 'xpto@terra.com.br',

        },
        {
            id: 004,
            name: 'Jordan',
            cidade: 'SC',
            email: 'xpto@terra.com.br',

        },
        {
            id: 004,
            name: 'Stephanie',
            cidade: 'SC',
            email: 'xpto@terra.com.br',

        },
        ]

        }
        }
    }
    </script>

    <style scoped>
    table {
        background: #ddd;
        border: #222;
    }

    .btn{
        width: 120px;
        height: 40px;
        border-radius: 10px;
        font-size: 18;
        letter-spacing: 1px;
        margin-left: 10px;
    }

    .btn-primary{
        background-color: blue;
        color:#ffff
    }

    </style> 