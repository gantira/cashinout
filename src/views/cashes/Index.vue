<template>
  <div class="container">
    <div class="w-full lg:w-8/12">
      <div>
        <div class="w-full mb-8">
          <div class="bg-gray-200 transform -rotate-2 rounded-2xl">
            <div
              class="bg-gradient-to-br from-blue-500 to-light-blue-400 text-white p-6 transform rotate-2 rounded-2xl"
            >
              <label
                class="block uppercase text-xs text-blue-100 fonsemi tracking-wider mb-2"
                >balances</label
              >
              <div class="text-3xl font-semibold">Rp {{ state.balances }}</div>
            </div>
          </div>
        </div>
        <div class="flex items-center -mx-2">
          <div class="w-full px-2">
            <div class="bg-gray-200 transform -rotate-3 rounded-2xl">
              <div
                class="bg-gradient-to-br from-teal-500 to-cyan-400 text-white p-6 transform rotate-3 rounded-2xl"
              >
                <label
                  class="block uppercase text-xs text-blue-100 fonsemi tracking-wider mb-2"
                  >debit</label
                >
                <div class="text-3xl font-semibold">Rp {{ state.debit }}</div>
              </div>
            </div>
          </div>
          <div class="w-full px-2">
            <div class="bg-gray-200 transform -rotate-3 rounded-2xl">
              <div
                class="bg-gradient-to-br from-red-500 to-yellow-400 text-white p-6 transform rotate-3 rounded-2xl"
              >
                <label
                  class="block uppercase text-xs text-blue-100 fonsemi tracking-wider mb-2"
                  >credit</label
                >
                <div class="text-3xl font-semibold">Rp {{ state.credit }}</div>
              </div>
            </div>
          </div>
        </div>

        <div class="my-10">
          <div class="border rounded-lg overflow-hidden">
            <div class="border-b px-6 py-4 bg-gray-50">Transaction</div>
            <div class="h-112 overflow-y-scroll">
              <template
                v-for="transaction in state.transactions"
                :key="transaction.id"
              >
                <a
                  href="#"
                  class="px-6 py-5 flex justify-between items-center border-b hover:bg-gray-100"
                >
                  <span class="flex flex-col">
                    <span class="text-100 text-xs">{{ transaction.when }}</span>
                    <span>{{ transaction.name }}</span>
                  </span>
                  <span
                    :class="
                      transaction.isCredit ? 'text-red-500' : 'text-green-500'
                    "
                    >{{ transaction.amount }}</span
                  >
                </a>
              </template>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { onMounted, ref } from "vue";
import axios from "axios";

export default {
  setup() {
    const state = ref([]);

    const getCashes = async () => {
      let { data } = await axios.get("api/cash");
      state.value = data;
    };

    onMounted(() => {
      getCashes();
    });

    return { getCashes, state };
  },
};
</script>

<style>
</style>