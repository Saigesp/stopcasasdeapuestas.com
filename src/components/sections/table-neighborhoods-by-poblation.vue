<template>
  <div>
    <table>
      <caption>Barrios según población y número de locales</caption>
      <thead>
        <tr>
          <td></td>
          <td></td>
          <td class="cen">0 locales</td>
          <td class="cen">1 local</td>
          <td class="cen">2-3 locales</td>
          <td class="cen">3-6 locales</td>
          <td class="cen">7+ locales</td>
          <td class="cen">Total</td>
        </tr>
      </thead>
      <tbody>
        <tr v-for="row in table">
          <td class="strong">{{row[0]}}</td>
          <td class="strong">{{row[1]}}</td>
          <td class="num">{{row[2]}}</td>
          <td class="num">{{row[3]}}</td>
          <td class="num">{{row[4]}}</td>
          <td class="num">{{row[5]}}</td>
          <td class="num">{{row[6]}}</td>
          <td class="num">{{row[7]}}</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td>Fuente: FRAVM</td>
        </tr>
      </tfoot>
    </table>

    <table>
      <caption>Residuos corregidos tipificados</caption>
      <thead>
        <tr>
          <td></td>
          <td class="cen">0 locales</td>
          <td class="cen">1 local</td>
          <td class="cen">2-3 locales</td>
          <td class="cen">3-6 locales</td>
          <td class="cen">7+ locales</td>
        </tr>
      </thead>
      <tbody>
        <tr v-for="row in table2">
          <td class="strong">{{row[0]}}</td>
          <td class="num">{{row[1]}}</td>
          <td class="num">{{row[2]}}</td>
          <td class="num">{{row[3]}}</td>
          <td class="num">{{row[4]}}</td>
          <td class="num">{{row[5]}}</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td>Fuente: FRAVM</td>
        </tr>
      </tfoot>
    </table>
  </div>
</template>


<script>
export default {
  name: 'table-neighborhoods-by-poblation',
  data: function(){
    return {
      table: [
        ["Muy bajo","Recuento",  '18,0',  '5,0',  '3,0',  '0,0',  '1,0',  '27,0'],
        ["","% Población",       '66,7', '18,5', '11,1',  '0,0',  '3,7', '100,0'],
        ["","% Locales",         '48,6', '20,8', '12,0',  '0,0',  '5,6',  '20,6'],
        ["Bajo","Recuento",      '11,0',  '7,0',  '7,0',  '2,0',  '1,0',  '28,0'],
        ["","% Población",       '39,3', '25,0', '25,0',  '7,1',  '3,6', '100,0'],
        ["","% Locales",         '29,7', '29,2', '28,0',  '7,4',  '5,6',  '21,4'],
        ["Medio","Recuento",      '4,0',  '5,0',  '5,0',  '7,0',  '5,0',  '26,0'],
        ["","% Población",       '15,4', '19,2', '19,2', '26,9', '19,2', '100,0'],
        ["","% Locales",         '10,8', '20,8', '20,0', '25,9', '27,8',  '19,8'],
        ["Alto","Recuento",       '3,0',  '5,0',  '5,0',  '9,0',  '3,0',  '25,0'],
        ["","% Población",       '12,0', '20,0', '20,0', '36,0', '12,0', '100,0'],
        ["","% Locales",          '8,1', '20,8', '20,0', '33,3', '16,7',  '19,1'],
        ["Muy alto","Recuento",   '1,0',  '2,0',  '5,0',  '9,0',  '8,0',  '25,0'],
        ["","% Población",        '4,0',  '8,0', '20,0', '36,0', '32,0', '100,0'],
        ["","% Locales",          '2,7',  '8,3', '20,0', '33,3', '44,4',  '19,1'],
        ["Total","Recuento",     '37,0', '24,0', '25,0', '27,0', '18,0', '131,0'],
        ["","% Población",       '28,2', '18,3', '19,1', '20,6', '13,7', '100,0'],
        ["","% Locales",        '100,0','100,0','100,0','100,0','100,0', '100,0'],
      ],
      table2: [
        ["Muy bajo","4,98","0,03","-1,18","-2,97","-1,70"],
        ["Bajo","1,46","1,03","0,90","-1,99","-1,76"],
        ["Medio","-1,63","0,13","0,02","0,89","0,91"],
        ["Alto","-2,01","0,24","0,13","2,11","-0,28"],
        ["Muy alto","-2,99","-1,48","0,13","2,11","2,95"],
      ]
    }
  }
}
</script>