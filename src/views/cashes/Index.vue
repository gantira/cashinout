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
              <div class="text-3xl font-semibold">Rp 1000.000</div>
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
                <div class="text-3xl font-semibold">Rp 1000.000</div>
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
                <div class="text-3xl font-semibold">Rp 1000.000</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mt-10">
          <div class="border rounded-lg overflow-hidden">
            <div class="border-b px-6 py-4 bg-gray-50">Transaction</div>
            <div class="px-6 py-4">
              <a
                href="#"
                class="flex justify-between items-center hover:bg-gray-50 p-4 rounded-lg hover:shadow mb-2"
              >
                <span class="flex flex-col">
                  <span class="text-100 text-xs">20 Nov 2020 15.33</span>
                  <span>Gaji Bulan November</span>
                </span>
                <span class="text-green-500">500.000</span>
              </a>
              <a
                href="#"
                class="flex justify-between items-center hover:bg-gray-50 p-4 rounded-lg hover:shadow"
              >
                <span class="flex flex-col">
                  <span class="text-gray-500 text-xs">20 Nov 2020 15.33</span>
                  <span>Beli Smartphone</span>
                </span>
                <span class="text-red-500">100.000</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>