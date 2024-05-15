<template>
    <header>
        <v-app-bar app dark color="yellow">
            <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
            <v-toolbar-title>ECサイト</v-toolbar-title>
            <v-slot>{{ today }}</v-slot>
            <!-- <v-tabs>
                <v-tab v-for="(menuItem, index) in headerItems" :key="index">
                    {{ menuItem.name }}
                </v-tab>
                
            </v-tabs> -->
        </v-app-bar>
        <v-navigation-drawer v-model="drawer" fixed temporary>
            <v-list nav dense>
                <v-list-item-group>
                    <v-list-item v-for="(sidebarItem, index) in sidebarItems" :key="index" :to="sidebarItem.url">
                        <v-list-item-title>{{ sidebarItem.name }}</v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </header>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      today: new Date(),
      sidebarItems: [
    {
      name: 'ホーム',
      url: '/home'
    },
    {
      name: 'ショッピング',
      url: '/shopping'
    },
    {
      name: 'カート',
      url: '/cart'
    },
    {
      name: 'ユーザー情報',
      url: '/user-info'
    },
    {
      name: '購入履歴',
      url: '/shopping-history'
    },
    {
      name: 'ログイン/ログアウト',
      url: '/login'
    }
  ],
      headerItems: [
    {
      name: 'ユーザー名',
      url: '#'
    },
    {
      name: '設定',
      url: '#'
    },
  ]
    }
  }
}

</script>
 
<style></style>