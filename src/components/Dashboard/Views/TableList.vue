<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <card>
            <template slot="header">
              <h4 class="card-title">Sum of revenue every hour</h4>
              <p class="card-category">Estimation based on produced H2</p>
            </template>
            <div class="table-responsive">
              <l-table class="table-hover table-striped"
                       :columns="table1.columns"
                       :data="table1.data">
              </l-table>
            </div>
          </card>

        </div>

        <div class="col-12">
          <card class="card-plain">
            <template slot="header">
              <h4 class="card-title">Table on Plain Background</h4>
              <p class="card-category">Here is a subtitle for this table</p>
            </template>
            <div class="table-responsive">
              <l-table class="table-hover"
                       :columns="table2.columns"
                       :data="table2.data">
              </l-table>
            </div>
          </card>
        </div>

      </div>
    </div>
  </div>
</template>
<script>
  import LTable from 'src/components/UIComponents/Table.vue'
  import Card from 'src/components/UIComponents/Cards/Card.vue'
  const tableColumns = ['Id', 'Time', 'Revenue', 'Diff_from_Yesterday']
  const tableData = [{
    id: 1,
    time: '9 am',
    revenue: '$36.738',
    diff_from_yesterday: '2 %'
  },
  {
    id: 2,
    time: '10 am',
    revenue: '$23,789',
    diff_from_yesterday: '3 %'
  },
  {
    id: 3,
    time: '11 am',
    revenue: '$56,142',
    diff_from_yesterday: '10 %'
  },
  {
    id: 4,
    time: '12 am',
    revenue: '$38,735',
    diff_from_yesterday: '1 %'
  },
  {
    id: 5,
    time: '13 pm',
    revenue: '$63,542',
    diff_from_yesterday: '0 %'
  }]
  const tableColumns2 = ['Id', 'Time', 'Average_active_H2_Station']
  const tableData2 = [{
    id: 1,
    time: '9 am',
    revenue: '$36.738',
    average_active_h2_station: '120'
  },
  {
    id: 2,
    time: '10 am',
    revenue: '$23,789',
    average_active_h2_station: '300'
  },
  {
    id: 3,
    time: '11 am',
    revenue: '$56,142',
    average_active_h2_station: '20'
  },
  {
    id: 4,
    time: '12 am',
    revenue: '$38,735',
    average_active_h2_station: '70'
  },
  {
    id: 5,
    time: '13 pm',
    revenue: '$63,542',
    average_active_h2_station: '110'
  }]
  export default {
    components: {
      LTable,
      Card
    },
    data () {
      return {
        table1: {
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          columns: [...tableColumns2],
          data: [...tableData2]
        }
      }
    }
  }
</script>
<style>
</style>
