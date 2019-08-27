<template>
  <div class="safa-grid" :class="onLoadAlign" style="height: 100vh;">
    <div class="button-row" style="margin-bottom: 5px;">
      <button @click="onRemoveSelected()">حذف انتخاب شده</button>
      <button @click="updateAndSort()">به روز رسانی</button>
      <button @click="addRow()">افزودن ردیف</button>
    </div>
    <ag-grid-vue
      class="ag-theme-balham"
      style=" height: calc(100% - 64px);"
      rowSelection="multiple"
      deltaRowDataMode="true"
      :gridOptions="gridOptions"
      :columnDefs="columnDefs"
      :rowData="rowData"
      :rowAnimation="true"
      :rowClassRules="rowClassRules"
      :getRowNodeId="getRowNodeId"
      @grid-ready="onGridReady"
    ></ag-grid-vue>
  </div>
</template>