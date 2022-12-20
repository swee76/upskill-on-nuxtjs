<template>
  <section>
    <div class="buttons">
      <b-button
        label="Rent"
        type="is-danger"
        size="is-medium"
        @click="isCardModalActive = true"
      />
    </div>

    <b-modal v-model="isCardModalActive" :width="540" scroll="keep">
      <div class="card">
        <div class="card-content">
          <div class="calendar-container">
            <div class="text-container">
              <div class="header">
                <div class="title">Using Component Methods</div>
                <b-button class="close-btn" @click="isCardModalActive = false"
                  ><b-icon pack="mdi" icon="window-close"></b-icon
                ></b-button>
              </div>
              <div class="content">
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Accusamus et illo sequi ipsa perspiciatis voluptas dicta eos
                  id nostrum sunt, voluptatibus impedit quaerat nisi
                  consequuntur earum dignissimos suscipit iure quia!
                </p>
                <vc-date-picker
                  :value="null"
                  color="indigo"
                  is-dark
                  is-range
                  :attributes="attrs"
                />
              </div>
              <b-button
                type="is-danger"
                size="is-medium"
                @click="
                  () => {
                    addItem(product.id);
                    isCardModalActive = false;
                  }
                "
                >Order</b-button
              >
            </div>
          </div>
        </div>
      </div>
    </b-modal>
  </section>
</template>

<script>
import { mapMutations } from "vuex";
export default {
  props: ["product"],
  data() {
    return {
      isCardModalActive: false,
      attrs: [
        {
          key: "today",
          highlight: true,
          dates: new Date(),
        },
      ],
    };
  },
  methods: {
    ...mapMutations(["addItem"]),
  },
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-bottom: 0.5rem;
  margin-bottom: 1rem;
  border-bottom: 2px solid rgb(158, 153, 153);
}

title {
  font-weight: bolder;
  font-size: large;
  margin: 0;
}
.buttons {
  width: 100%;
  border: none;
  color: white;
  font-weight: 700;
  color: white;
  font-weight: 700;
  transition: 0.5s;
}

.button {
  width: 100%;
  border-radius: 100rem;
  margin: 1rem 0;
}

.close-btn {
  border: none;
  width: fit-content;
  margin-bottom: 2rem;
}
.calendar-container {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
p {
  color: grey;
}
.text-container {
  padding: 0.5rem;
}
.content {
  display: flex;
}
</style>
