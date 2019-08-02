
Internacionalizacion
Puede cambiar el texto en los paneles de paginación y los filtros predeterminados proporcionando un localeText o un localeTextFunc a gridOptions.

Usando localeText
El siguiente ejemplo muestra todo el texto que se puede definir. con un jemplo en español

var columnDefs = [
    // this row just shows the row index, doesn't use any data from the row
    {headerName: "#", width: 50, cellRenderer:  'rowNodeIdRenderer'},
    {headerName: "Athlete", field: "athlete", width: 150},
    {headerName: "Age", field: "age", width: 90},
    {headerName: "Country", field: "country", width: 120},
    {headerName: "Year", field: "year", width: 90, filter: 'agNumberColumnFilter'},
    {headerName: "Date", field: "date", width: 110},
    {headerName: "Sport", field: "sport", width: 110, filter: 'agTextColumnFilter'},
    {headerName: "Gold", field: "gold", width: 100},
    {headerName: "Silver", field: "silver", width: 100},
    {headerName: "Bronze", field: "bronze", width: 100, enableRowGroup: true, enablePivot: true, enableValue:true, pivot: true},
    {headerName: "Total", field: "total", width: 100}
];

var gridOptions = {
    defaultColDef: {
        sortable: true,
        resizable: true,
        filter: true
    },
    // note - we do not set 'virtualPaging' here, so the grid knows we are doing standard paging
    components:{
        rowNodeIdRenderer: function(params) {
            return params.node.id + 1;
        }
    },
    columnDefs: columnDefs,
    sideBar: true,
    pagination:true,
    rowGroupPanelShow: 'always',
    statusBar: {
        items: [
            { component: 'agAggregationComponent' }
        ]
    },
    paginationPageSize: 500,
    enableRangeSelection: true,
    enableCharts: true,
    localeText: {
      // for filter panel
      page: 'Pagina',
      more: 'Mas',
      to: 'a',
      of: 'de',
      next: 'Siguente',
      last: 'Último',
      first: 'Primero',
      previous: 'Anteror',
      loadingOoo: 'Cargando...',

      // for set filter
      selectAll: 'Seleccionar Todo',
      searchOoo: 'Buscar...',
      blanks: 'En blanco',

      // for number filter and text filter
      filterOoo: 'Filtrar',
      applyFilter: 'Aplicar Filtro...',
      equals: 'Igual',
      notEqual: 'No Igual',

      // for number filter
      lessThan: 'Menos que',
      greaterThan: 'Mayor que',
      lessThanOrEqual: 'Menos o igual que',
      greaterThanOrEqual: 'Mayor o igual que',
      inRange: 'En rango de',

      // for text filter
      contains: 'Contiene',
      notContains: 'No contiene',
      startsWith: 'Empieza con',
      endsWith: 'Termina con',

      // filter conditions
      andCondition: 'Y',
      orCondition: 'O',

      // the header of the default group column
      group: 'Grupo',

      // tool panel
      columns: 'Columnas',
      filters: 'Filtros',
      valueColumns: 'Valos de las Columnas',
      pivotMode: 'Modo Pivote',
      groups: 'Grupos',
      values: 'Valores',
      pivots: 'Pivotes',
      toolPanelButton: 'BotonDelPanelDeHerramientas',

      // other
      noRowsToShow: 'No hay filas para mostrar',

      // enterprise menu
      pinColumn: 'Columna Pin',
      valueAggregation: 'Agregar valor',
      autosizeThiscolumn: 'Autoajustar esta columna',
      autosizeAllColumns: 'Ajustar todas las columnas',
      groupBy: 'agrupar',
      ungroupBy: 'desagrupar',
      resetColumns: 'Reiniciar Columnas',
      expandAll: 'Expandir todo',
      collapseAll: 'Colapsar todo',
      toolPanel: 'Panel de Herramientas',
      export: 'Exportar',
      csvExport: 'Exportar a CSV',
      excelExport: 'Exportar a Excel (.xlsx)',
      excelXmlExport: 'Exportar a Excel (.xml)',


      // enterprise menu pinning
      pinLeft: 'Pin Izquierdo',
      pinRight: 'Pin Derecho',


      // enterprise menu aggregation and status bar
      sum: 'Suman',
      min: 'Minimo',
      max: 'Maximo',
      none: 'nada',
      count: 'contar',
      average: 'promedio',

      // standard menu
      copy: 'Copiar',
      copyWithHeaders: 'Copiar con cabeceras',
      paste: 'Pegar'   
  }
  
    }
