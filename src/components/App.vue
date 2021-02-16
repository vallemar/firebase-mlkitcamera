<template>
  <Page>
    <ActionBar title="Welcome to NativeScript-Vue!"/>
    <GridLayout columns="*" rows="*">
      <BottomNavigation>
        <TabContentItem>
          <Label text="HOME"></Label>
        </TabContentItem>
        <TabContentItem>
          <Frame>
            <Scan></Scan>
          </Frame>
        </TabContentItem>
        <TabStrip>
          <TabStripItem>
            <Label text="HOME"></Label>
          </TabStripItem>
          <TabStripItem>
            <Label text="SCAN"></Label>
          </TabStripItem>
        </TabStrip>
      </BottomNavigation>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import Scan from "@/components/Scan.vue";

export default {
  components: {Scan},
  data() {
    return {

      msg: 'Hello World!'
    }
  }
}
</script>

<style scoped>
ActionBar {
  background-color: #53ba82;
  color: #ffffff;
}

.message {
  vertical-align: center;
  text-align: center;
  font-size: 20;
  color: #333333;
}
</style>
