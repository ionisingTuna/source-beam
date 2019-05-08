<template>
    <Page class="page">
        <ActionBar class="action-bar">
            <Label class="action-bar-title" text="Home"></Label>
        </ActionBar>

        <StackLayout verticalAlignment="center">
            <Button horizontalAlignment="center" text="Toggle" @tap="set" /></Button>
        </StackLayout>
    </Page>
</template>

<script>
  import * as flashlight from "nativescript-flashlight";
    export default {
        computed: {
            message() {
                return "Toggle.";
            }
        },
        data () {
          return {
          toggle: true
          }
        },
        methods: {
          set: function () {
              
              flashlight.toggle({
              intensity: 0.25
            });
            /*var brightness = new nativescriptBrightness.Brightness();
            const brightness = new Brightness();
              brightness.set({
             intensity: 25
          });
          */
          }
        }
    };
</script>

<style scoped lang="scss">
    // Start custom common variables
    @import '../app-variables';
    // End custom common variables

    // Custom styles
    .fa {
        color: $accent-dark;
    }

    .info {
        font-size: 20;
    }
</style>
