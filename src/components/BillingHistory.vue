<template>
    <div class="bg-white">
        <h5>Billing history</h5>
        <p>Choose a billing plan to see more details</p>
    </div>
    
    <table class="table table-hover bg-white">
  <thead>
    <tr>
      <th scope="col">Date</th>
      <th scope="col">Type</th>
      <th scope="col">Amount</th>
      <th scope="col">Balance</th>
      <th scope="col">Reference</th>
      <th scope="col">Download</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(item, index) in history" :key="index">
      <th scope="row">{{formatDate(item.date) }} </th>
      <td>{{item.type}}</td>
      <td>£{{ item.amount }}</td>
      <td>£{{ item.balance }}</td>
      <td>{{item.reference}}</td>
      <td>
        <button class="btn">
           <BIconDownload class="text-primary" />
        </button>
       
      </td>
      
    </tr>


  </tbody>
</table>
</template>

<script>
import { BIconDownload} from 'bootstrap-icons-vue'

export default {
    components: {
        BIconDownload
    },
    props: ['formatDate'],
      data () {
    return {
      history: [
        {
          date: new Date(2021, 11, 13),
          type:'Invoice',
          amount:8,
          balance:45,
          reference:'8993UDEJ',
          downloadLink:''
          },
          {
          date: new Date(2021, 11, 13),
          type:'Invoice',
          amount:8,
          balance:45,
          reference:'8993UDEJ',
          downloadLink:''
          }
      ]
    }
  }
}
</script>