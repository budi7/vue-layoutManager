# vue-layoutManager
componnet to helps you manage page/component state (loading, error, nodata, and showing datas)


## Installation 
clone/download and place it on your components folder

## Registration

    import layoutManager from '~/components/layoutManager'
    
    components: {
      layoutManager
    }
    
## Parameter
    
    isError: state when error (Boolean)
    isEmpty: state when no data (Boolean)
    isLoading: state when loading (Boolean)
    
    
## Slots 

    error: this section will be shown when error state is true
    empty: this section will be shown when empty / no data state is true
    loader: this section will be shown when loading state is true
    content: this section will be shown when error state, empty, and loading state is false
    
    
## Examples

    <layoutManager
      :is-loading="isPageLoading"
      :is-error="isPageError"
      :is-empty="PageDatas.length === 0"
      class="w-100"
    >
      <template #empty>
        Empty
      </template>
      <template #error>
        Error
      </template>
      <template #loader>
        Loading
      </template>
      <template #content>
        Showing Page Data
      </template>
    </layoutmanager>

  
