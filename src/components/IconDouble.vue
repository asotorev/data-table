Component for two state boxes: 
Checkbox Icon, Filter Icon, Highlighter Icon

<template>
    <label>
        <input type="checkbox" :class="className">
        <span class="check-toggle"></span>
    </label>
</template>

<script>
export default {
    props: ['className']
}
</script>

<style scoped>
    input[type='checkbox'] {
        position: absolute;
        left: -10000px;
        top: auto;
        height: 0;
        width: 0;
        overflow: hidden;
    }
    input[type='checkbox'].border ~ .check-toggle {
        /* border: 2px solid #ACD9E3; */
        /* border: 2px solid #FFAAAA; */
        border: 2px solid #FFD400;
        vertical-align: middle;
    }
    input[type='checkbox'] ~ .check-toggle {
        width: 32px;
        height: 32px;
        box-sizing: border-box;
        position: relative;
        display: inline-block;
        background: white;
        border-radius: 10%;
        cursor: pointer;
    }
    /* Checkbox Icon */
    input[type='checkbox']:hover ~ .check-toggle {
        /* border-color: #87C0CD; */
        /* border-color: #FF8162; */
        border-color: #F8B500;
    }
    input[type='checkbox'].check-icon:checked ~ .check-toggle {
        background: center/60% no-repeat white url("data:image/svg+xml,%3Csvg width='19' height='16' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M2 10.4L5.46153846 14 17 2' stroke='%23F8B500' stroke-width='3' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");  
    }
    /* Filter Icon */
    input[type='checkbox'].filter-icon ~ .check-toggle {
        background: center/60% no-repeat white url("data:image/svg+xml,%3Csvg width='22' height='21' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%23EBEBEB' fill-rule='evenodd'%3E%3Cpath d='M8.91 12v8.1c0 .23.13.43.33.54a.64.64 0 0 0 .64-.03l1.37-.88 2.17-1.62c.17-.16.13-.16.13-.29V12l6.92-7.98-9.22.05c-6.31-.11-9.4-.09-9.24.08L8.9 12z'/%3E%3Cpath d='M11 .38C.33.38.33 1.84.33 2.04v2.48c0 .28 3.08 2.1 10.67 2.1s10.67-1.82 10.67-2.1V2.04c0-.28 0-1.66-10.67-1.66z'/%3E%3C/g%3E%3C/svg%3E");
    }
    input[type='checkbox'].filter-icon:checked ~ .check-toggle {
        background: center/60% no-repeat white url("data:image/svg+xml,%3Csvg width='22' height='21' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cpath d='M8.91 12v8.1c0 .23.13.43.33.54a.64.64 0 0 0 .64-.03l1.37-.88 2.17-1.62c.17-.16.13-.16.13-.29V12l6.92-7.98-9.22.05c-6.31-.11-9.4-.09-9.24.08L8.9 12z' fill='%235D7486'/%3E%3Cpath d='M2 4.15l.34.38L8.9 12v8.1c0 .23.13.43.33.54a.64.64 0 0 0 .64-.03l1.37-.88V4.07c-6.31-.11-9.4-.09-9.24.08z' fill='%237CAED6'/%3E%3Cpath d='M11 .38C.33.38.33 1.84.33 2.04v2.48c0 .28 3.08 2.1 10.67 2.1s10.67-1.82 10.67-2.1V2.04c0-.28 0-1.66-10.67-1.66z' fill='%2334536B'/%3E%3Cpath d='M11.25.37C.58.37.33 1.77.33 2.04v2.49c0 .27 2.43 2.08 10.92 2.08V.37z' fill='%234783B2'/%3E%3Cellipse fill='%2334536B' cx='11' cy='1.5' rx='10' ry='1.5'/%3E%3C/g%3E%3C/svg%3E");
    }  
    /* Highlighter Icon */
    input[type='checkbox'].marker-icon ~ .check-toggle {
        background: center/65% no-repeat white url("data:image/svg+xml,%3Csvg viewBox='0 0 28 26' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M26.28 6.89L21 1.68a3.04 3.04 0 0 0-3.64-.27L3.97 13.43a.77.77 0 0 0-.22.82l1.4 4.11-4.67 4.28c-.32.28-.27.63 0 .98.42.3 4.53 2.2 4.79 2.32.46.18.78-.3 1.01-.51 1-.9 1.63-1.48 1.88-1.74l1.2-1.18 4.18 1.37a.8.8 0 0 0 .83-.22L26.55 10.6a2.9 2.9 0 0 0-.27-3.7z' fill='%23EBEBEB' fill-rule='evenodd'/%3E%3C/svg%3E");
    }
    input[type='checkbox'].marker-icon:checked ~ .check-toggle {
        background: center/65% no-repeat white url("data:image/svg+xml,%3Csvg viewBox='0 0 27 25' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill-rule='evenodd'%3E%3Cpath d='M26.1 5.75L21.17.88A3.09 3.09 0 0 0 18.98 0a3.1 3.1 0 0 0-2.08.78L5.27 11.26a.77.77 0 0 0-.03 1.12l9.18 9.03a.8.8 0 0 0 .56.23h.01a.8.8 0 0 0 .57-.25L26.2 9.94a3.03 3.03 0 0 0-.1-4.2z' fill='%23FFD400'/%3E%3Cpath d='M26.1 5.75L23.65 3.3 9.83 16.9l4.59 4.51a.8.8 0 0 0 .56.23h.01a.8.8 0 0 0 .57-.25L26.2 9.94a3.03 3.03 0 0 0-.1-4.2z' fill='%23F8B500'/%3E%3Cpath d='M15.54 20.31l-9.18-9.03a.8.8 0 0 0-1.1-.02l-1.29 1.17a.77.77 0 0 0-.22.82l1.4 4.1-1.2 1.2a.77.77 0 0 0 0 1.1l3.1 3.04a.8.8 0 0 0 1.11 0l1.2-1.18 4.18 1.37a.8.8 0 0 0 .83-.22l1.19-1.27a.77.77 0 0 0-.02-1.08z' fill='%23EFF6FE'/%3E%3Cpath d='M10.95 15.8l-5.46 5.37 1.55 1.52a.8.8 0 0 0 1.12 0l1.2-1.18 4.18 1.37a.8.8 0 0 0 .83-.22l1.19-1.27a.77.77 0 0 0-.02-1.08l-4.6-4.51z' fill='%23D2DCE7'/%3E%3Cpath d='M4.87 18.52l3.12 3.34c.27.3.3.7.07.91l-2.22 2.08c-.16.14-.4.17-.64.05L.74 22.8a.87.87 0 0 1-.45-.52c-.07-.23-.02-.44.12-.58l3.56-3.32c.23-.2.63-.15.9.14z' fill='%23F8B500'/%3E%3Cpath d='M6.43 20.2l-1.56-1.68c-.27-.29-.67-.35-.9-.14L.41 21.7c-.14.14-.19.35-.12.58.07.22.24.42.45.52l1.92.9 3.77-3.5z' fill='%23FFD400'/%3E%3C/g%3E%3C/svg%3E");
    }
</style>

