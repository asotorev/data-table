
<template>
  <!-- https://bc-payments-data.firebaseio.com/ -->
  <table>
    <colgroup>
        <col style="width:5%">
    </colgroup>
    <thead>
      <tr id="table-title">
        <th colspan="6">
          <div id="test">
            <p>Payments Data</p>
            <input class="search">
          </div>
        </th>
      </tr>
      <tr id="headers">
        <th></th>
        <th v-for="(header, index) in headers" :key="index">
          {{ header }}
        </th>
      </tr>
      <tr id="icons">
        <th><app-icon-double className="marker-icon"/></th> 
        <th v-for="(header, index) in headers" :key="index">
          <app-icon-triple 
            :name="'sort' + index" 
            :id1="'off' + index" 
            :id2="'up' + index" 
            :id3="'down' + index"/>
          <app-icon-double className="filter-icon"/>
        </th>
      </tr>
      <tr>
        <th></th>
        <th v-for="(header, index) in headers" :key="index">
          <input class="search">
        </th>
      </tr>
    </thead>
    <tr>
    </tr>
    <tr>
      <td class="check">
        <app-icon-double className="check-icon border"/>
      </td>
      <td>E624450C-EACE-C049-A094-AEA22E62DF2B</td>
      <td>Alfreds Futterkiste</td>
      <td>ac libero nec ligula consectetuer rhoncus. Nullam velit dui, semper</td>
      <td>2018-10-01T08:03:47-07:00</td>
      <td class="amount">285.6</td>
    </tr>
    <tr>
      <td class="check">
        <app-icon-double className="check-icon border"/>
      </td>
      <td>E624450C-EACE-C049-A094-AEA22E62DF2B</td>
      <td>Alfreds Futterkiste</td>
      <td>ac libero nec ligula consectetuer rhoncus. Nullam velit dui, semper</td>
      <td>2018-10-01T08:03:47-07:00</td>
      <td class="amount">285.6</td>
    </tr>
    <tr>
      <td colspan="6" style="text-align:right">
          <span class="plus-icon"></span>
      </td>
    </tr>
    
  </table>

</template>

<script>
  import IconDouble from './components/IconDouble.vue'
  import IconTriple from './components/IconTriple.vue'
  
  export default {
    components : {
      appIconDouble: IconDouble,
      appIconTriple: IconTriple,
    }, 
    data() {
      return{
        headers: ['Id','Name','Description','Date','Amount'],
      }
    },

  }
</script>

<style>

  @import url('https://fonts.googleapis.com/css?family=Poppins');

  body {
    font-family: 'Poppins', sans-serif;
    font-size: 10px;
    letter-spacing: 0.05em;
    color: #5D7486;
    margin: 0;
    background-color: #F9F9F9;
  }

  table {
    border-collapse: collapse;
    width: 100%;
  }

  thead tr:not(:first-child){
    background: #EBEBEB;
    text-align: center;
    padding: 8px;
    font-size: 12px;
  }

  #table-title{
    text-align: left; 
    background: #268EA5;
    /* background: #F8B500; */
    /* background: #2F5179; */
    color: white;
    font-size: 18px;
  }

  #table-title *{
    margin: 0;
  }

  #table-title th{
    padding: 0px 16px;
  }

  #headers th{
    padding: 8px 8px 0 8px;
    min-width: 20px;
    color: #268EA5;
  }

  #icons th{
    padding: 8px;
    min-width: 75px;
  }
  
  td{
    border: 1px solid #EBEBEB;
    background: white;
    padding: 4px;
    /* vertical-align: middle; */
    /* max-width: 100px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap; */
  }

  tr:hover td{
    /* background-color: #F9F9F9; */
    background-color: #F0F0F0;
    /* background-color: #FFEA84; */
    border: 1px solid white;
  }
  
  .search{
    margin: 0 0 8px 0;
    padding-left: 24px;
    box-sizing: border-box;
    border: none;
    background-image: url("data:image/svg+xml,%3Csvg width='22' height='22' xmlns='http://www.w3.org/2000/svg'%3E%3Cg transform='translate(2 2)' stroke='%23ACD9E3' stroke-width='3' fill='none' fill-rule='evenodd' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='8' cy='8' r='8'/%3E%3Cpath d='M18 18l-4.3-4.3'/%3E%3C/g%3E%3C/svg%3E");
    background-position: 5px 4px; 
    background-repeat: no-repeat;
    border-radius: 15px;
    height: 24px;
    width: 100%;
    max-width: 200px;
    background-size: 16px;
    outline: none;
    color: #5D7486;
  }
  
  img {
    display: inline-block;
    width: 32px;
    cursor: pointer;
  }

  #test{
    padding: 10px 0;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .check {
    text-align: center;
  }

  .plus-icon{
    margin-right: 14px;
    vertical-align: middle;
    width: 32px;
    height: 32px;
    position: relative;
    display: inline-block;
    box-sizing: border-box;
    border-radius: 10%;
    border: 2px solid #ACD9E3;
    cursor: pointer;
    background: center/70% no-repeat white url("data:image/svg+xml,%3Csvg width='18' height='18' xmlns='http://www.w3.org/2000/svg'%3E%3Cg stroke='%23ACD9E3' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M9 1.8v14.4M2 9.4h14'/%3E%3C/g%3E%3C/svg%3E");
  }

  .plus-icon:hover{
   border-color: #87C0CD; 
  }
  
  .amount{
    text-align: right;
    padding-right: 16px;
  }

</style>
