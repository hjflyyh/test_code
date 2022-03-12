<template>
  
</template>

<script>
import { defineComponent } from '@vue/composition-api'
import ApolloClient from "apollo-boost";
import VueApollo from "vue-apollo";
Vue.use(VueApollo);

import CyberConnect, { Env, Blockchain } from "@cyberlab/cyberconnect";

const cyberConnect = new CyberConnect({
  namespace: "CyberConnect",
  chain: Blockchain.ETH,
  provider: provider,
});

const apolloClient = new ApolloClient({
  uri: "http://localhost:4000/graphql"
});

const apolloProvider = new VueApollo({
  defaultClient: apolloClient
});

new Vue({
  router,
  apolloProvider,
  render: h => h(App)
}).$mount('#app')

cyberConnect.connect(targetAddr);



export default defineComponent({
  setup() {
    
  },
})
</script>




<style lang="scss">

</style>
