<template>
  <Page actionBarHidden="true" iosOverflowSafeArea="false">
    <GridLayout iosOverflowSafeArea="false">

      <MLKitBarcodeScanner
          ref="refMLKitBarcodeScanner"
          width="100%"
          height="100%"
          class="border-props"
          beepOnScan="false"
          formats="CODE_128, CODE_39,CODE_93, CODABAR, DATA_MATRIX,EAN_13, EAN_8, ITF,QR_CODE,UPC_A,UPC_E,PDF417,ZTEC"
          preferFrontCamera="false"
          supportInverseBarcodes="false"
      >
      </MLKitBarcodeScanner>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import * as permissions from "nativescript-permissions";

export default {
  name: "Scan",
  created() {
    permissions
        .requestPermission(
            android.Manifest.permission.CAMERA,
            "I need these permissions"
        )
        .then(() => {
          this.okPermission = true;
        })
        .finally(() => (this.responsePermission = true))
        .catch(() => console.log("ERROR PERMISION"));
  }
}
</script>

<style scoped>

</style>