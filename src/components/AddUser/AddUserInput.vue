<template>
  <form ref="form" class="w-full p-4" @submit.prevent="createUser()">
    <!-- name -->
    <div class="floating-input mb-5 relative">
      <input
        type="text"
        id="name"
        name="name"
        class="
          border border-gray-200
          focus:outline-none
          rounded-md
          focus:border-gray-500 focus:shadow-sm
          w-full
          p-3
          h-16
        "
        placeholder=" "
        autocomplete="off"
        v-model="name"
      />
      <label
        for="email"
        class="
          absolute
          top-0
          right-0
          px-3
          py-5
          h-full
          pointer-events-none
          transform
          origin-left
          transition-all
          duration-100
          ease-in-out
        "
        >الاسم</label
      >
    </div>

    <!-- email -->
    <div class="floating-input mb-5 relative">
      <input
        type="text"
        id="name"
        name="email"
        class="
          border border-gray-200
          focus:outline-none
          rounded-md
          focus:border-gray-500 focus:shadow-sm
          w-full
          p-3
          h-16
        "
        placeholder=" "
        autocomplete="off"
        v-model="name"
      />
      <label
        for="email"
        class="
          absolute
          top-0
          right-0
          px-3
          py-5
          h-full
          pointer-events-none
          transform
          origin-left
          transition-all
          duration-100
          ease-in-out
        "
        >االايميل</label
      >
    </div>

    <!-- phone -->
    <div class="floating-input mb-5 relative">
      <input
        type="number"
        id="phone"
        name="tel"
        class="
          border border-gray-200
          focus:outline-none
          rounded-md
          focus:border-gray-500 focus:shadow-sm
          w-full
          p-3
          h-16
        "
        placeholder=" "
        autocomplete="off"
        v-model="phone"
      />
      <label
        for="phone"
        class="
          absolute
          top-0
          right-0
          px-3
          py-5
          h-full
          pointer-events-none
          transform
          origin-left
          transition-all
          duration-100
          ease-in-out
        "
      >
        رقم الهاتف</label
      >
    </div>

    <!-- country -->
    <div class="floating-input mb-5 relative">
      <input
        type="password"
        id="name"
        name="password"
        class="
          border border-gray-200
          focus:outline-none
          rounded-md
          focus:border-gray-500 focus:shadow-sm
          w-full
          p-3
          h-16
        "
        placeholder=" "
        autocomplete="off"
        v-model="name"
      />
      <label
        for="email"
        class="
          absolute
          top-0
          right-0
          px-3
          py-5
          h-full
          pointer-events-none
          transform
          origin-left
          transition-all
          duration-100
          ease-in-out
        "
        >كلمه السر</label
      >
    </div>

    <!-- password -->
    <div class="floating-input mb-5 relative">
      <input
        type="text"
        id="contry"
        name="password"
        class="
          border border-gray-200
          focus:outline-none
          rounded-md
          focus:border-gray-500 focus:shadow-sm
          w-full
          p-3
          h-16
        "
        placeholder=" "
        autocomplete="off"
        v-model="country"
      />
      <label
        for="contry"
        class="
          absolute
          top-0
          right-0
          px-3
          py-5
          h-full
          pointer-events-none
          transform
          origin-left
          transition-all
          duration-100
          ease-in-out
        "
        >الدوله</label
      >
    </div>

    <!-- address -->
    <div class="floating-input mb-5 relative">
      <input
        type="text"
        id="address"
        name="address"
        class="
          border border-gray-200
          focus:outline-none
          rounded-md
          focus:border-gray-500 focus:shadow-sm
          w-full
          p-3
          h-16
        "
        placeholder=" "
        autocomplete="off"
        v-model="address"
      />
      <label
        for="address"
        class="
          absolute
          top-0
          right-0
          px-3
          py-5
          h-full
          pointer-events-none
          transform
          origin-left
          transition-all
          duration-100
          ease-in-out
        "
        >العنوان
      </label>
    </div>

    <!-- image -->
    <div class="image my-2">
      <label for="image"> صورة المستخدم </label>
      <div class="flex justify-center items-center w-full">
        <label
          for="dropzone-file"
          class="
            flex flex-col
            justify-center
            items-center
            w-full
            h-64
            bg-gray-50
            rounded-lg
            border-2 border-gray-300 border-dashed
            cursor-pointer
            dark:hover:bg-bray-800 dark:bg-gray-700
            hover:bg-gray-100
            dark:border-gray-600
            dark:hover:border-gray-500
            dark:hover:bg-gray-600
          "
        >
          <div class="flex flex-col justify-center items-center pt-5 pb-6">
            <svg
              aria-hidden="true"
              class="mb-3 w-10 h-10 text-gray-400"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"
              ></path>
            </svg>
            <p class="mb-2 text-sm text-gray-500 dark:text-gray-400">
              <span class="font-semibold">Click to upload</span> or drag and
              drop
            </p>
            <p class="text-xs text-gray-500 dark:text-gray-400">
              SVG, PNG, JPG or GIF (MAX. 800x400px)
            </p>
          </div>
          <input id="dropzone-file" type="file" class="hidden" />
        </label>
      </div>
    </div>

    <!-- role -->
    <label
      for="countries"
      class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-400"
    >
      نوع المستخدم
    </label>
    <select
      id="countries"
      name="role"
      class="
        bg-gray-50
        border border-gray-300
        text-gray-900 text-sm
        rounded-lg
        focus:ring-black focus:border-black
        block
        w-full
        p-2.5
        dark:bg-gray-700
        dark:border-gray-600
        dark:placeholder-gray-400
        dark:text-white
        dark:focus:ring-blue-500
        dark:focus:border-blue-500
      "
    >
      <option value="admin">مشرف</option>
      <option value="vendor">تاجر</option>
    </select>

    <!-- button -->
    <div class="checkout py-2">
      <button class="bg-blue-600 px-4 py-2 text-white rounded">
        اضف المستخدم
      </button>
    </div>
  </form>
</template>

<script>
export default {
  name: "AddUserInput",
  methods: {
    createUser() {
      const formData = new FormData(this.$refs.form);
      this.$store.dispatch("createUser", formData);
      this.success = true;
    },
  },
};
</script>

<style>
</style>