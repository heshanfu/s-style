<style lang="scss" scoped>
</style>

<template>
  <div>
    <h3> Buttons </h3>
    <p> Buttons are selectable elements that allow a user to trigger other actions.</p>
    <demo :code="button1Template">
      <s-button>Button</s-button>
      <s-button :disabled="true">Disabled Button</s-button>
      <s-button :selected="true">Selected Button</s-button>
    </demo>
    <demo :code="button2Template">
      <s-button color="primary">Button</s-button>
      <s-button color="primary" :disabled="true">Disabled Button</s-button>
      <s-button color="primary" :selected="true">Selected Button</s-button>
    </demo>
    <demo :code="button3Template">
      <s-button color="success">Button</s-button>
      <s-button color="success" :disabled="true">Disabled Button</s-button>
      <s-button color="success" :selected="true">Selected Button</s-button>
    </demo>
    <demo :code="button4Template">
      <s-button color="error">Button</s-button>
      <s-button color="error" :disabled="true">Disabled Button</s-button>
      <s-button color="error" :selected="true">Selected Button</s-button>
    </demo>
    <options :items="buttonItems"></options>
  </div>
</template>

<script>
import demo from "../../components/demo.vue";
import options from "../../components/options.vue";

export default {
  components: {
    demo,
    options
  },
  data() {
    return {
      button1Template: `
<template>
    <s-button>Button</s-button>
    <s-button :disabled="true">Disabled Button</s-button>
    <s-button :selected="true">Selected Button</s-button>
</template>`,
      button2Template: `
<template>
    <s-button color="primary">Button</s-button>
    <s-button color="primary" :disabled="true">Disabled Button</s-button>
    <s-button color="primary" :selected="true">Selected Button</s-button>
</template>`,
      button3Template: `
<template>
    <s-button color="success">Button</s-button>
    <s-button color="success" :disabled="true">Disabled Button</s-button>
    <s-button color="success" :selected="true">Selected Button</s-button>
</template>`,
      button4Template: `
<template>
    <s-button color="error">Button</s-button>
    <s-button color="error" :disabled="true">Disabled Button</s-button>
    <s-button color="error" :selected="true">Selected Button</s-button>
</template>`,
      buttonItems: {
        Props: [
          {
            name: "disabled",
            type: "Boolean",
            default: "false",
            required: "",
            description: "Disable interaction with the alert."
          },
          {
            name: "selected",
            type: "Boolean",
            default: "false",
            required: "",
            description: "Is the block selected?"
          },
          {
            name: "color",
            type: "String",
            default: "",
            required: "",
            description:
              "Default color of the button ('', primary, success, error)"
          }
        ],
        Slots: [
          {
            name: "",
            scope: "",
            description: "Manually set the view of the button"
          }
        ],
        Events: []
      }
    };
  }
};
</script>