<template>
      <div>
            <div class="nav"></div>
            <div class="container mx-auto">
                  <h1 class=" my-3 w-96 display-in bg-slate-500">{{ title }}</h1>
                  <div class="my-4 w-96 bg-orange-300">
                        <select class="py-2" name="sort" id="sort">
                              <option value="">Giá từ cao đến thấp</option>
                              <option value="">Giá từ thấp đến cao</option>
                        </select>
                  </div>
                  <hr>
            </div>
      </div>
</template>
<script>
export default {
      setup() {
            const title = "Tất cả các sản phẩm";
            const data = fetch('https://fakestoreapi.com/products')
                  .then((response) => response.json())
                  .then((data) => console.log(data));
            // console.log(data.title(0) + "dbhcbdhbh");
            return { title, data };
      },
};
</script>
