<template>
<div>
<h1> {{hello}}</h1>
<label for="> {{name}} </label><br>
<input type="text v-model="name">

<section v=if"isTrue">
    <AlunoTable />
<table>
    <tr>
        <td>Nome</td>
        <td>Email</td>
        <td>Cidade</td>
        <td>Ações</td>
    </tr>
    <tr>
        <td>XPTO</td>
        <td>XPTO</td>
        <td>XPTO</td>
        <td>
        <button class="btn btn-primary"> Adicionar </button>
        <button class="btn btn-danger"> Remover </button>
        
        </td>
         
    </tr>
</table>
</section>

<section v-if="isTrue">
<p>Não tem dados</p>
</section>
</div>
</template>

<script>

export default {
    name: 'AlunoTemplate',
    data(){
        return{
          name: '',
          hello> 'Alexandre',
            isTrue: true,
        };
    },

};

</script>

<style>
table{
    background: #ddd;
    border: #222;
}

.btn{
    width: 120px;
    height: 40px;
    border-radius: 10px;
    font-size: 18px;
    letter-spacing: 1px;
    margin-left: 10px;

}
.btn-primary{
    background-color: blue;
    color:#fff;
}

.btn-danger{
    background-color: red;
    color: #fff;
}

</style>

