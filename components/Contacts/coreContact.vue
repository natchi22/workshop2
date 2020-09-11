<template>
  <div class="tb-contact">
    <a-table
      :columns="columns"
      :data-source="data"
      :row-selection="rowSelection"
      :pagination="false"
    >
      <template slot="name" slot-scope="text, record">
        <div class="col-name">
          <img :src="record.image" alt="">
          <p>{{ text }}</p>
        </div>
      </template>
    </a-table>
  </div>
</template>
<script>
const columns = [
  {
    title: 'Name',
    dataIndex: 'name',
    key: 'name',
    scopedSlots: { customRender: 'name' }
  },
  {
    title: 'E-mail',
    dataIndex: 'email',
    key: 'email'
  },
  {
    title: 'Company name',
    dataIndex: 'companyName',
    key: 'companyName'
  },
  {
    title: 'Role',
    dataIndex: 'role',
    key: 'role'
  },
  {
    title: 'Forecast',
    dataIndex: 'forecast',
    key: 'forecast'
  },
  {
    title: 'RecentActivity',
    dataIndex: 'recentActivity',
    key: 'recentActivity',
    align: 'right'
  }
]

const data = [
  {
    key: 1,
    image: require('~/assets/images/layout/01.png'),
    name: 'Lindsey Stroud',
    email: 'lindsey.stroud@gmail.com',
    companyName: 'Hatchbuck',
    role: 'Manager',
    forecast: '50 %',
    recentActivity: '5 Minutes ago'
  },
  {
    key: 2,
    image: require('~/assets/images/layout/02.png'),
    name: 'Nicci Troiani',
    email: 'nicci.troiani@gmail.com',
    companyName: 'Slack',
    role: 'Manager',
    forecast: '75 %',
    recentActivity: '14 Minutes ago'
  },
  {
    key: 3,
    image: require('~/assets/images/layout/03.png'),
    name: 'George Fields',
    email: 'george.fields@gmail.com',
    companyName: 'Clockify',
    role: 'CEO',
    forecast: '10 %',
    recentActivity: '6 Hours ago'
  },
  {
    key: 4,
    image: require('~/assets/images/layout/04.png'),
    name: 'Rebecca Moore',
    email: 'rebecca.moore@gmail.com',
    companyName: 'Upwork',
    role: 'Manager',
    forecast: '25 %',
    recentActivity: 'Dec 14, 2018'
  },
  {
    key: 5,
    image: require('~/assets/images/layout/05.png'),
    name: 'Jane Doe',
    email: 'jane.doe@gmail.com',
    companyName: 'Trello',
    role: 'Engineer',
    forecast: '30 %',
    recentActivity: 'Dec 12, 2018'
  },
  {
    key: 6,
    image: require('~/assets/images/layout/06.png'),
    name: 'Jones Dermot',
    email: 'dermot.jones@gmail.com',
    companyName: 'Slack',
    role: 'Developer',
    forecast: '40 %',
    recentActivity: 'Dec 11, 2018'
  },
  {
    key: 7,
    image: require('~/assets/images/layout/07.png'),
    name: 'Martin Merces',
    email: 'martin.merces@gmail.com',
    companyName: 'Google',
    role: 'Manager',
    forecast: '60 %',
    recentActivity: 'Dec 9, 2018'
  },
  {
    key: 8,
    image: require('~/assets/images/layout/08.png'),
    name: 'Franz Ferdinand',
    email: 'franz.ferdiand@gmail.com',
    companyName: 'Facebook',
    role: 'Manager',
    forecast: '100 %',
    recentActivity: 'Dec 6, 2018'
  },
  {
    key: 9,
    image: require('~/assets/images/layout/09.png'),
    name: 'John Smith',
    email: 'john.smith@gmail.com',
    companyName: 'Skype',
    role: 'CEO',
    forecast: '75 %',
    recentActivity: 'Nov 30, 2018'
  },
  {
    key: 10,
    image: require('~/assets/images/layout/10.png'),
    name: 'Judith Williams',
    email: 'judith.williams@gmail.com',
    companyName: 'Google',
    role: 'Designer',
    forecast: '45 %',
    recentActivity: 'Nov 26, 2018'
  }
]

const rowSelection = {
  onChange: (selectedRowKeys, selectedRows) => {
    // console.log(`selectedRowKeys: ${selectedRowKeys}`, 'selectedRows: ', selectedRows)
  },
  onSelect: (record, selected, selectedRows) => {
    // console.log(record, selected, selectedRows)
  },
  onSelectAll: (selected, selectedRows, changeRows) => {
    // console.log(selected, selectedRows, changeRows)
  }
}

export default {
  data () {
    return {
      data,
      columns,
      rowSelection
    }
  }
}
</script>
<style>
.ant-pagination .ant-table-pagination {
    display: none;
}
.ant-table-thead > tr > th{
  color: #334D6E;
  opacity: 0.5;
  padding: 20px 24px 20px 24px;
  background-color: #ffffff;
}
.ant-table{
  font-weight: 500;
  font-size: 13px;
  line-height: 19px;
  color: #707683;
}
.ant-table-tbody > tr > td > .col-name > p{
  color: #323C47;
  font-size: 15px;
  line-height: 22px;
  margin: 0 0 0 12px;
}
.ant-table-tbody > tr > td.ant-table-selection-column {
  text-align: left;
}
.col-name{
  display: flex;
}
.col-name img{
  width: 24px;
  height: 24px;
}
.ant-table-tbody > tr > td{
  padding: 20px 0 20px 24px ;
  cursor: pointer;
}
.ant-table-tbody > tr:hover{
  box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.1);
  background-color: #ffffff !important;
}
.ant-table-tbody > tr > td:last-child{
  padding-right: 24px ;
}
.ant-table-tbody > tr > td:first-child{
  padding-right: 0 ;
}
.ant-table table{
  box-shadow: 0px 6px 18px rgba(0, 0, 0, 0.06) ;
  border-radius: 4px;
}
@media screen and (max-width: 1279px ) and (min-width: 768px ){
/* .tb-contact{
  width: 1000px;
} */
}
@media screen and (max-width: 767px){
/* .tb-contact{
  width: 1000px;
} */
}
</style>
