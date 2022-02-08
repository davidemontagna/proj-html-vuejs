<template>
    
    <div class="search-box d-flex align-items-center">
        <input type="text" class="search-input" placeholder="Search..">
        <a class="search-btn" href="#">
            <!-- Seach Icon -->
            <i class="fas fa-search"></i>
        </a>
    </div>
    
            
</template>

<script>
export default {
    name: 'SearchBar',
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.search-box {  
  background: $bg-color-1;
  height: 40px;
  border-radius: 50px;
  padding: 10px;  
}
.search-box:hover{
    border: 1px solid $border-color-10;
}
/* input */
.search-input {
  outline: none;
  border: none;
  background: none;
  width: 0;
  padding: 0;
  color: $font-color-10;
  float: left;
  font-size: 16px;
  transition: .3s;
  line-height: 40px;
}
.search-input::placeholder {
  color: $font-color-10;
}
/* icon */
.search-btn {
  color: $font-color-10;
  float: right;  
  border-radius: 50px;  
  display: flex;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  transition: .3s;
}
.search-input:focus,
.search-input:not(:placeholder-shown) {
  width: 240px;
  padding: 0 10px;
}
.search-box:hover > .search-input {
  width: 240px;
  padding: 0px 6px;
}
.search-box:hover > .search-btn,
.search-input:focus + .search-btn,
.search-input:not(:placeholder-shown) + .search-btn {
  background: $bg-color-1;
  color: $font-color-10;
}

</style>