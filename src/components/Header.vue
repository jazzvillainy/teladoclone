<template>
  <div class="">
    <!-- <div class="top-bar-left">
      <ul class="menu" role="presentation">
        <li class="menu-text navigation-item--logo" role="presentation">
          <a aria-label="Logo Teladoc Home" href="/">Teladoc</a>
        </li>
      </ul>
    </div>
    <div>
      <div></div>
      <div>ENG</div>
    </div> -->
    <header>
      <nav>
        <div class="container">
            
          <img style="width:11%; height:11%" src="https://s3.amazonaws.com/images.teladoc.com/member/Logo-Horz-RGB.svg" alt="">
          <ul class="nav-links" @mouseover="handleMouseover">
            <li style="display:flex; align-items:center">
              <img
                src="data:image/svg+xml;charset=utf-8;base64,PHN2ZyB3aWR0aD0iNTUiIGhlaWdodD0iNTQiIHZpZXdCb3g9IjAgMCA1NSA1NCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgZmlsdGVyPSJ1cmwoI2ZpbHRlcjBfZF85MDM1XzY4MDMxKSI+CjxyZWN0IHg9IjUuNSIgeT0iNCIgd2lkdGg9IjQ0IiBoZWlnaHQ9IjQ0IiByeD0iMjIiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0yNy41IDE3Ljk5OTlDMjMuMDgwNiAxNy45OTk5IDE5LjUgMjEuNTgwNSAxOS41IDI1Ljk5OTlDMTkuNSAzMC40MTkyIDIzLjA4MDYgMzMuOTk5OSAyNy41IDMzLjk5OTlDMzEuOTE5NCAzMy45OTk5IDM1LjUgMzAuNDE5MiAzNS41IDI1Ljk5OTlDMzUuNSAyMS41ODA1IDMxLjkxOTQgMTcuOTk5OSAyNy41IDE3Ljk5OTlaTTMzLjI3NDIgMjMuMTYxMkgzMS4xMTI5QzMwLjg4NzEgMjEuOTk5OSAzMC41MzIzIDIwLjk2NzYgMzAuMDgwNiAyMC4xMjg5QzMxLjQ2NzcgMjAuNzQxOCAzMi41OTY4IDIxLjgwNjMgMzMuMjc0MiAyMy4xNjEyWk0yNy41IDE5LjU0ODNDMjguMDgwNiAxOS41NDgzIDI5LjA0ODQgMjAuOTAzMSAyOS41MzIzIDIzLjE2MTJIMjUuNDM1NUMyNS45MTk0IDIwLjkwMzEgMjYuODg3MSAxOS41NDgzIDI3LjUgMTkuNTQ4M1pNMjEuMDQ4NCAyNS45OTk5QzIxLjA0ODQgMjUuNTgwNSAyMS4wODA2IDI1LjEyODkgMjEuMTc3NCAyNC43MDk2SDIzLjY2MTNDMjMuNjI5IDI1LjE2MTIgMjMuNjI5IDI1LjU4MDUgMjMuNjI5IDI1Ljk5OTlDMjMuNjI5IDI2LjQ1MTUgMjMuNjI5IDI2Ljg3MDggMjMuNjYxMyAyNy4yOTAySDIxLjE3NzRDMjEuMDgwNiAyNi45MDMxIDIxLjA0ODQgMjYuNDUxNSAyMS4wNDg0IDI1Ljk5OTlaTTIxLjY5MzUgMjguODM4NkgyMy44NTQ4QzI0LjA4MDYgMzAuMDMyMSAyNC40MzU1IDMxLjA2NDQgMjQuODg3MSAzMS45MDMxQzIzLjUgMzEuMjkwMiAyMi4zNzEgMzAuMTkzNCAyMS42OTM1IDI4LjgzODZaTTIzLjg1NDggMjMuMTYxMkgyMS42OTM1QzIyLjM3MSAyMS44MDYzIDIzLjUgMjAuNzQxOCAyNC44ODcxIDIwLjEyODlDMjQuNDM1NSAyMC45Njc2IDI0LjA4MDYgMjEuOTk5OSAyMy44NTQ4IDIzLjE2MTJaTTI3LjUgMzIuNDUxNUMyNi44ODcxIDMyLjQ1MTUgMjUuOTE5NCAzMS4xMjg5IDI1LjQzNTUgMjguODM4NkgyOS41MzIzQzI5LjA0ODQgMzEuMTI4OSAyOC4wODA2IDMyLjQ1MTUgMjcuNSAzMi40NTE1Wk0yOS43NTgxIDI3LjI5MDJIMjUuMjA5N0MyNS4xNzc0IDI2LjkwMzEgMjUuMTc3NCAyNi40NTE1IDI1LjE3NzQgMjUuOTk5OUMyNS4xNzc0IDI1LjU0ODMgMjUuMTc3NCAyNS4xMjg5IDI1LjIwOTcgMjQuNzA5NkgyOS43NTgxQzI5Ljc5MDMgMjUuMTI4OSAyOS44MjI2IDI1LjU0ODMgMjkuODIyNiAyNS45OTk5QzI5LjgyMjYgMjYuNDUxNSAyOS43OTAzIDI2LjkwMzEgMjkuNzU4MSAyNy4yOTAyWk0zMC4wODA2IDMxLjkwMzFDMzAuNTMyMyAzMS4wNjQ0IDMwLjg4NzEgMzAuMDMyMSAzMS4xMTI5IDI4LjgzODZIMzMuMjc0MkMzMi41OTY4IDMwLjE5MzQgMzEuNDY3NyAzMS4yOTAyIDMwLjA4MDYgMzEuOTAzMVpNMzEuMzA2NSAyNy4yOTAyQzMxLjMzODcgMjYuODcwOCAzMS4zNzEgMjYuNDUxNSAzMS4zNzEgMjUuOTk5OUMzMS4zNzEgMjUuNTgwNSAzMS4zMzg3IDI1LjE2MTIgMzEuMzA2NSAyNC43MDk2SDMzLjgyMjZDMzMuODg3MSAyNS4xMjg5IDMzLjk1MTYgMjUuNTgwNSAzMy45NTE2IDI1Ljk5OTlDMzMuOTUxNiAyNi40NTE1IDMzLjg4NzEgMjYuOTAzMSAzMy44MjI2IDI3LjI5MDJIMzEuMzA2NVoiIGZpbGw9IiM1NjU3NTciLz4KPHJlY3QgeD0iNiIgeT0iNC41IiB3aWR0aD0iNDMiIGhlaWdodD0iNDMiIHJ4PSIyMS41IiBzdHJva2U9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxmaWx0ZXIgaWQ9ImZpbHRlcjBfZF85MDM1XzY4MDMxIiB4PSIwLjUiIHk9IjAiIHdpZHRoPSI1NCIgaGVpZ2h0PSI1NCIgZmlsdGVyVW5pdHM9InVzZXJTcGFjZU9uVXNlIiBjb2xvci1pbnRlcnBvbGF0aW9uLWZpbHRlcnM9InNSR0IiPgo8ZmVGbG9vZCBmbG9vZC1vcGFjaXR5PSIwIiByZXN1bHQ9IkJhY2tncm91bmRJbWFnZUZpeCIvPgo8ZmVDb2xvck1hdHJpeCBpbj0iU291cmNlQWxwaGEiIHR5cGU9Im1hdHJpeCIgdmFsdWVzPSIwIDAgMCAwIDAgMCAwIDAgMCAwIDAgMCAwIDAgMCAwIDAgMCAxMjcgMCIgcmVzdWx0PSJoYXJkQWxwaGEiLz4KPGZlTW9ycGhvbG9neSByYWRpdXM9IjEiIG9wZXJhdG9yPSJkaWxhdGUiIGluPSJTb3VyY2VBbHBoYSIgcmVzdWx0PSJlZmZlY3QxX2Ryb3BTaGFkb3dfOTAzNV82ODAzMSIvPgo8ZmVPZmZzZXQgZHk9IjEiLz4KPGZlR2F1c3NpYW5CbHVyIHN0ZERldmlhdGlvbj0iMiIvPgo8ZmVDb2xvck1hdHJpeCB0eXBlPSJtYXRyaXgiIHZhbHVlcz0iMCAwIDAgMCAwIDAgMCAwIDAgMCAwIDAgMCAwIDAgMCAwIDAgMC4wOCAwIi8+CjxmZUJsZW5kIG1vZGU9Im5vcm1hbCIgaW4yPSJCYWNrZ3JvdW5kSW1hZ2VGaXgiIHJlc3VsdD0iZWZmZWN0MV9kcm9wU2hhZG93XzkwMzVfNjgwMzEiLz4KPGZlQmxlbmQgbW9kZT0ibm9ybWFsIiBpbj0iU291cmNlR3JhcGhpYyIgaW4yPSJlZmZlY3QxX2Ryb3BTaGFkb3dfOTAzNV82ODAzMSIgcmVzdWx0PSJzaGFwZSIvPgo8L2ZpbHRlcj4KPC9kZWZzPgo8L3N2Zz4K"
                alt=""
              />
              <span><b>ENG</b></span>
            </li>
          </ul>
        </div>
      </nav>
    </header>
  <DropDown />
  </div>
</template>

<script>
import "primeicons/primeicons.css";
import DropDown from './DropDown.vue'
export default {
    components:{DropDown}
};
</script>

<style scoped>
header {
  background-color: #fff;
  /* box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); */
  padding: 1.3rem 0;
  border-bottom: 1px solid;
  margin: 0% 5%;
}



.container {
  display: flex;
  justify-content: space-between;
  padding-left: 5%;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

/* .logo {
  font-weight: bold;
  font-size: 1.5rem;
  text-decoration: none;
  color: #333;
} */

.nav-links {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.nav-links li {
  margin-left: 2rem;
}

.nav-links a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
}

.nav-links a:hover {
  text-decoration: underline;
}
</style>
