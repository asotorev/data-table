Component for three state boxes: 
Sort Icon

<template>
    <span class="radio-opts">
        <input type="radio" :id="id1" :name="name" value="off" checked>
        <label :for="id2" ></label>
        <input type="radio" :id="id2" :name="name" value="asc">
        <label :for="id3" ></label>
        <input type="radio" :id="id3" :name="name" value="desc" >
        <label :for="id1"></label>
    </span>    
</template>

<script>
    export default {
        props: ['name', 'id1', 'id2', 'id3']
    }   
</script>

<style scoped>
  input[type='radio']:checked + label {
    position: relative;
    display: inline-block;
    width: 32px;
    height: 32px;
    border-radius: 10%;
  }
  input[type='radio'] {
    display: none;
  }
  input[value="off"] + label {
    background: center/70% no-repeat white url("data:image/svg+xml,%3Csvg width='22' height='16' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M9.25 1.65L.61 12.75a1.26 1.26 0 0 0 0 1.57 2.2 2.2 0 0 0 1.74.8h17.3c.72-.02 1.39-.32 1.75-.8.36-.49.36-1.08 0-1.57l-8.65-11.1A2.23 2.23 0 0 0 11 .89c-.71 0-1.38.29-1.75.76z' fill='%23EBEBEB' fill-rule='evenodd'/%3E%3C/svg%3E");
  }
  input[value="asc"] + label {
    background: center/70% no-repeat white url("data:image/svg+xml,%3Csvg width='22' height='16' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cpath d='M9.25 1.65L.61 12.75a1.26 1.26 0 0 0 0 1.57 2.2 2.2 0 0 0 1.74.8h17.3c.72-.02 1.39-.32 1.75-.8.36-.49.36-1.08 0-1.57l-8.65-11.1A2.23 2.23 0 0 0 11 .89c-.71 0-1.38.29-1.75.76z' fill='%23268EA5'/%3E%3Cpath d='M9.25 1.65L.61 12.75a1.26 1.26 0 0 0 0 1.57 2.2 2.2 0 0 0 1.74.8H11V.88c-.71 0-1.38.29-1.75.76z' fill='%2387C0CD'/%3E%3C/g%3E%3C/svg%3E");    
  }
  input[value="desc"] + label {
    background: center/70% no-repeat white url("data:image/svg+xml,%3Csvg width='25' height='14' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cpath d='M14.55 13.26L24.68 2.32a1.1 1.1 0 0 0 0-1.54C24.27.3 23.49.01 22.64 0H2.37C1.52 0 .74.3.3.78a1.1 1.1 0 0 0 .01 1.54l10.13 10.94c.44.46 1.21.74 2.05.74.84 0 1.61-.28 2.05-.74z' fill='%23FF8162'/%3E%3Cpath d='M12.5 0H2.27C1.46 0 .71.3.3.78c-.4.48-.4 1.06 0 1.54l9.74 10.94c.41.46 1.66.74 2.46.74V0z' fill='%23FAA'/%3E%3C/g%3E%3C/svg%3E");
  }
  .radio-opts { 
    -webkit-touch-callout: none; /* iOS Safari */
      -webkit-user-select: none; /* Safari */
      -moz-user-select: none; /* Firefox */
      -ms-user-select: none; /* Internet Explorer/Edge */
      user-select: none; /* Non-prefixed version, currently supported by Chrome and Opera */
    }                                
</style>
