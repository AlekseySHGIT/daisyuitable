<template >
  <!-- Open the modal using ID.showModal() method -->
  <button class="btn" onclick="my_modal_1.showModal()">open modal</button>
  <dialog id="my_modal_1" class="modal">
    <form method="dialog" class="modal-box">
      <h3 class="font-bold text-lg">Hello!</h3>
      <p class="py-4">Press ESC key or click the button below to close</p>
      <div class="modal-action">
        <!-- if there is a button in form, it will close the modal -->
        <button class="btn">Close</button>
      </div>
    </form>
  </dialog>
  <div class="container mx-auto  flex overflow-x-auto card bg-base-300 w-80">
    <div class="card-body">
      <input placeholder="Email" class="input input-bordered" />
      <label class="label cursor-pointer">
        Accept terms of use
        <input type="checkbox" class="toggle" />
      </label>
      <label class="label cursor-pointer">
        Submit to newsletter
        <input type="checkbox" class="toggle" />
      </label>
      <button class="btn btn-neutral">Save</button>
    </div>
  </div>

  <h1 className="text-3xl font-bold underline">
    Hello world!
  </h1>
  <button class="btn">Button</button>
  <button class="btn btn-primary">Button</button>
  <div class="container mx-auto  flex overflow-x-auto">
    <table class="table">
      <!-- head -->
      <thead>
      <tr>


        <th>Column 1</th>
        <th>Column 2</th>
        <th>Column 3</th>
        <th>Column 4</th>
        <th>Column 5</th>
        <th>Column 6</th>

      </tr>
      </thead>
      <tbody >
      <!-- row 1 -->
      <tr v-for= "(oneDesert,i) in desserts" :key="i">

        <td v-for= "(oneElem,j) in oneDesert" :key="j">
          {{ oneElem }}
        </td>


      </tr>

      </tbody>
    </table>
  </div>
</template>

<script>

export default {
  data () {
    return {
      itemsPerPage: 5,
      headers: [
        {
          title: 'Dessert (100g serving)',
          align: 'start',
          sortable: false,
          key: 'name',
        },
        { title: 'Calories', align: 'end', key: 'calories' },
        { title: 'Fat (g)', align: 'end', key: 'fat' },
        { title: 'Carbs (g)', align: 'end', key: 'carbs' },
        { title: 'Protein (g)', align: 'end', key: 'protein' },
        { title: 'Iron (%)', align: 'end', key: 'iron' },
      ],
      myelements:[
          '21321',
          '453436453',
          '234234324',
          '435634643'
      ],
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1',
        },
        {
          name: 'Jelly bean',
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: '0',
        },
        {
          name: 'KitKat',
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          iron: '6',
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7',
        },
        {
          name: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: '16',
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1',
        },
        {
          name: 'Lollipop',
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: '2',
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8',
        },
        {
          name: 'Honeycomb',
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: '45',
        },
        {
          name: 'Donut',
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: '22',
        },
      ],
    }
  },
}
</script>