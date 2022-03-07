<template>
  <div
    class="p-10 px-4 mx-auto max-w-4xl h-screen"
    id="appp"
    style="z-index: 0"
  >
    <div class="flex items-center justify-center">
      <img
        alt="ineedmore.domains logo"
        src="../assets/logos/vector/default.svg"
        class="w-screen"
      />
    </div>
    <br />
    <div class="flex items-center justify-center h-10 w-full">
      <h2 class="text-2xl font-semibold text-white">Domain Search</h2>
    </div>
    <br />
    <div class="flex items-center justify-center h-10 w-full">
      <h3 class="text-2xl text-white">Choose the registrar you want to use:</h3>
    </div>
    <br />
    <div class="grid grid-flow-row lg:grid-cols-4 gap-4 w-full">
      <div class="flex p-2 px-8 bg-white rounded-lg text-sm h-24">
        <a
          :href="
            'https://porkbun.com/checkout/search?q=' + this.$route.query.search
          "
          class="w-full h-full justify-center items-center flex"
          ><img
            src="https://porkbun.design/images/porkbun_rgb.svg"
            alt="Porkbun"
            class="h-1/3"
        /></a>
      </div>
      <div class="flex p-2 px-8 bg-white rounded-lg text-sm h-24">
        <a
          :href="
            'https://www.namecheap.com/domains/registration/results/?domain=' +
            this.$route.query.search
          "
          class="w-full h-full justify-center items-center flex"
        >
          <img
            src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2aWV3Qm94PSIwIDAgMjU4IDQ2LjU3Ij48ZGVmcz48bGluZWFyR3JhZGllbnQgaWQ9ImEiIHgxPSI1OS45OSIgeTE9IjQ0LjE2IiB4Mj0iODAuMDEiIHkyPSIxLjIzIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSI+PHN0b3Agb2Zmc2V0PSIwIiBzdG9wLWNvbG9yPSIjZDQyMDJjIi8+PHN0b3Agb2Zmc2V0PSIwLjEiIHN0b3AtY29sb3I9IiNkYzNkMjkiIHN0b3Atb3BhY2l0eT0iMC43OSIvPjxzdG9wIG9mZnNldD0iMC4yIiBzdG9wLWNvbG9yPSIjZTQ1OTI2IiBzdG9wLW9wYWNpdHk9IjAuNTgiLz48c3RvcCBvZmZzZXQ9IjAuMzIiIHN0b3AtY29sb3I9IiNlYTcxMjMiIHN0b3Atb3BhY2l0eT0iMC40Ii8+PHN0b3Agb2Zmc2V0PSIwLjQzIiBzdG9wLWNvbG9yPSIjZjA4NTIxIiBzdG9wLW9wYWNpdHk9IjAuMjUiLz48c3RvcCBvZmZzZXQ9IjAuNTUiIHN0b3AtY29sb3I9IiNmNDk0MWYiIHN0b3Atb3BhY2l0eT0iMC4xNCIvPjxzdG9wIG9mZnNldD0iMC42OCIgc3RvcC1jb2xvcj0iI2Y3OWYxZSIgc3RvcC1vcGFjaXR5PSIwLjA2Ii8+PHN0b3Agb2Zmc2V0PSIwLjgyIiBzdG9wLWNvbG9yPSIjZjhhNTFkIiBzdG9wLW9wYWNpdHk9IjAuMDIiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNmOWE3MWQiIHN0b3Atb3BhY2l0eT0iMCIvPjwvbGluZWFyR3JhZGllbnQ+PGxpbmVhckdyYWRpZW50IGlkPSJiIiB4MT0iMTc3Ny40OCIgeTE9IjEwNDguNzYiIHgyPSIxNzk3LjUiIHkyPSIxMDA1LjgzIiBncmFkaWVudFRyYW5zZm9ybT0idHJhbnNsYXRlKDE4MDMuNSAxMDUyLjYpIHJvdGF0ZSgxODApIiB4bGluazpocmVmPSIjYSIvPjwvZGVmcz48dGl0bGU+Y24tbG9nbzwvdGl0bGU+PHBhdGggZD0iTTc3LjE3LjcxYTcuODcsNy44NywwLDAsMC02Ljg4LDQuMDVsLS4xNi4zM0w2NCwxNy4yNWwtNy44LDE1LjM3LDUuMTEsMTAuMDcuMjguNTVBOCw4LDAsMCwwLDY1LDQ2LjQ3YTguMDUsOC4wNSwwLDAsMCwzLjQxLTMuMjNsLjI4LS41NUw4NCwxMi40OGwuMzctLjczYTcuODYsNy44NiwwLDAsMC03LjE5LTExWiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTEgLTAuNzEpIiBmaWxsPSIjZmY1MTAwIi8+PHBhdGggZD0iTTI5Ljg1LDE1LjM0bC01LjEtMTAtLjI4LS41NWE3Ljg5LDcuODksMCwwLDAtMy40LTMuMjIsNy45Miw3LjkyLDAsMCwwLTMuNCwzLjIxbC0uMjkuNTZMMi4wNSwzNS41MmwtLjM3LjcyYTcuODYsNy44NiwwLDAsMCwxNC4wNiw3bC4xNy0uMzIsNi4xNy0xMi4xNkwyOS44NywxNS40WiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTEgLTAuNzEpIiBmaWxsPSIjZmY1MTAwIi8+PHBhdGggZD0iTTc3LjE1LjcxYTcuODYsNy44NiwwLDAsMC02Ljg3LDQuMDVsLS4xNy4zM0w2My45NCwxNy4yNSw1Ni4xMywzMi42Mmw1LjEyLDEwLjA3LjI4LjU1YTcuOTQsNy45NCwwLDAsMCwzLjQxLDMuMjMsNy45NCw3Ljk0LDAsMCwwLDMuNDEtMy4yM2wuMjktLjU1TDg0LDEyLjQ4bC4zNi0uNzNhNy44Niw3Ljg2LDAsMCwwLTcuMTktMTFaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMSAtMC43MSkiIGZpbGw9InVybCgjYSkiLz48cGF0aCBkPSJNOC44Niw0Ny4yOWE3Ljg2LDcuODYsMCwwLDAsNi44Ny00bC4xNy0uMzMsNi4xOC0xMi4xNiw3LjgtMTUuMzdMMjQuNzcsNS4zMWwtLjI4LS41NWE4LDgsMCwwLDAtMy40Mi0zLjIzLDgsOCwwLDAsMC0zLjQxLDMuMjNsLS4yOC41NUwyLDM1LjUybC0uMzcuNzNhNy44Niw3Ljg2LDAsMCwwLDcuMTksMTFaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMSAtMC43MSkiIGZpbGw9InVybCgjYikiLz48cGF0aCBkPSJNMjkuODUsMTUuMzRsLTUuMS0xMC0uMjgtLjU1YTcuOTQsNy45NCwwLDAsMC0zLjQxLTMuMjNBOC4zMSw4LjMxLDAsMCwxLDIyLjU1LDFhOC4xNiw4LjE2LDAsMCwxLDItLjI1SDM1LjIzYTcuOTIsNy45MiwwLDAsMSw2Ljg2LDRsLjI4LjU1TDU2LjE4LDMyLjY2bDUuMDksMTAsLjI4LjU1QTgsOCwwLDAsMCw2NSw0Ni40N2E4LjA1LDguMDUsMCwwLDEtMy40Ny44MUg1MC43OWE3LjkxLDcuOTEsMCwwLDEtNi44NS00bC0uMjktLjU1WiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTEgLTAuNzEpIiBmaWxsPSIjZmY4YzQ0Ii8+PHBhdGggZD0iTTk4LDI0LjUzYS43Ni43NiwwLDAsMSwuODQtLjg0aC42YS43NS43NSwwLDAsMSwuOC44NHYxLjk0YTUuNzUsNS43NSwwLDAsMS0uMTMsMS4yMWguMDdhNy40Myw3LjQzLDAsMCwxLDYuOC00LjM5YzQuMTksMCw1LjY2LDIuMzgsNS42Niw2LjUzdjkuODlhLjc2Ljc2LDAsMCwxLS44NC44NGgtLjYzYS43NC43NCwwLDAsMS0uODEtLjg0VjMwLjQzYzAtMi42NS0uNDMtNS0zLjY4LTUtMy41OSwwLTYuNCwyLjk1LTYuNCw2Ljg4djcuNGEuNzQuNzQsMCwwLDEtLjgxLjg0aC0uNjNhLjc2Ljc2LDAsMCwxLS44NC0uODRaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMSAtMC43MSkiIGZpbGw9IiM2ZTZmNzEiLz48cGF0aCBkPSJNMTI0Ljg5LDMwLjIzaDF2LS41NGMwLTMuMjUtMS43OC00LjM2LTQuMTYtNC4zNmE4LDgsMCwwLDAtNC4wOSwxLjE4Ljc5Ljc5LDAsMCwxLTEuMTMtLjI3bC0uMjEtLjM0YS43Ni43NiwwLDAsMSwuMjQtMS4xNCwxMC4zNCwxMC4zNCwwLDAsMSw1LjM2LTEuNDdjNCwwLDYuMjcsMi4yNCw2LjI3LDYuNDd2MTBhLjc0Ljc0LDAsMCwxLS44MS44NGgtLjUzYS43NS43NSwwLDAsMS0uODQtLjg0VjM4LjM3YTcuMTQsNy4xNCwwLDAsMSwuMS0xLjI3SDEyNkE2LjI1LDYuMjUsMCwwLDEsMTIwLjMsNDFjLTIuODUsMC01LjctMS42Ny01LjctNC45MkMxMTQuNiwzMC41MywxMjEuNjQsMzAuMjMsMTI0Ljg5LDMwLjIzWk0xMjAuNywzOWMzLjI1LDAsNS4xNi0zLjM1LDUuMTYtNi4zdi0uOGgtLjk0Yy0yLjY1LDAtOCwuMS04LDMuODhDMTE2Ljk0LDM3LjQsMTE4LjE5LDM5LDEyMC43LDM5WiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTEgLTAuNzEpIiBmaWxsPSIjNmU2ZjcxIi8+PHBhdGggZD0iTTEzMS4zOSwyNC41M2EuNzYuNzYsMCwwLDEsLjg0LS44NGguNmEuNzUuNzUsMCwwLDEsLjguODR2MS45NGE1Ljc1LDUuNzUsMCwwLDEtLjEzLDEuMjFoLjA3YTcuMTUsNy4xNSwwLDAsMSw2LjItNC4zOWMzLjExLDAsNC43MiwxLjQ0LDUuMTksNC4yMkgxNDVhNy4xNiw3LjE2LDAsMCwxLDYuMi00LjIyYzQuMDksMCw1LjU5LDIuMzgsNS41OSw2LjUzdjkuODlhLjc2Ljc2LDAsMCwxLS44My44NGgtLjYxYS43Ni43NiwwLDAsMS0uODQtLjg0VjMwLjM5YzAtMi43NC0uNTYtNS0zLjYxLTUtMy4zOSwwLTUuNjcsMy41NS01LjY3LDd2Ny4zYS43My43MywwLDAsMS0uOC44NGgtLjY0YS43Ni43NiwwLDAsMS0uODQtLjg0VjMwLjM5YzAtMi41NC0uMzctNS0zLjU1LTUtMy40MiwwLTUuNzYsMy42Mi01Ljc2LDd2Ny4zYS43NC43NCwwLDAsMS0uODEuODRoLS42M2EuNzYuNzYsMCwwLDEtLjg0LS44NFoiIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0xIC0wLjcxKSIgZmlsbD0iIzZlNmY3MSIvPjxwYXRoIGQ9Ik0xNjcuMjgsMjMuMjljNC40OSwwLDcsMy4yNSw3LDhhLjg0Ljg0LDAsMCwxLS44OC44NEgxNjEuMzFjLjEsNC4yOSwzLjA1LDYuNzQsNi41NCw2Ljc0YTcuMTcsNy4xNywwLDAsMCw0LjQyLTEuNTUuNy43LDAsMCwxLDEuMTEuMmwuMjcuNDFhLjc4Ljc4LDAsMCwxLS4yNCwxLjFBOS41MSw5LjUxLDAsMCwxLDE2Ny43OCw0MSw4LjUxLDguNTEsMCwwLDEsMTU5LDMyLjE0QzE1OSwyNi42MSwxNjIuNzIsMjMuMjksMTY3LjI4LDIzLjI5Wk0xNzIsMzAuNDZjLS4xNC0zLjU1LTIuMjgtNS4zLTQuOC01LjNhNS44Miw1LjgyLDAsMCwwLTUuOCw1LjNaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMSAtMC43MSkiIGZpbGw9IiM2ZTZmNzEiLz48cGF0aCBkPSJNMTg1LjE3LDIzLjI5YTguODQsOC44NCwwLDAsMSw1LjYsMS45MS43Mi43MiwwLDAsMSwuMSwxLjE0bC0uMjMuMzdjLS4zLjQ3LS42Ny40Ny0xLjE0LjE3YTcsNywwLDAsMC00LjI2LTEuNTUsNi41LDYuNSwwLDAsMC02LjU3LDYuODEsNi41LDYuNSwwLDAsMCw2LjYsNi43N0E3LjM1LDcuMzUsMCwwLDAsMTkwLDM3LjEzYS42Ny42NywwLDAsMSwxLjExLjJsLjIzLjM0YS44LjgsMCwwLDEtLjIsMS4xMyw5LjMyLDkuMzIsMCwwLDEtNiwyLjE1LDguNTMsOC41MywwLDAsMS04Ljg0LTguODFBOC41OSw4LjU5LDAsMCwxLDE4NS4xNywyMy4yOVoiIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0xIC0wLjcxKSIgZmlsbD0iIzZlNmY3MSIvPjxwYXRoIGQ9Ik0xOTMuNjUsMTcuODNhLjczLjczLDAsMCwxLC44LS44NGguNjRhLjc2Ljc2LDAsMCwxLC44NC44NHY4LjQxYTcuMTgsNy4xOCwwLDAsMS0uMTMsMS4zN2guMDZhNy40Myw3LjQzLDAsMCwxLDYuNzQtNC4zMmM0LjE5LDAsNS42NiwyLjM4LDUuNjYsNi41M3Y5Ljg5YzAsLjU0LS4yNi44NC0uOC44NGgtLjY0YS43Ni43NiwwLDAsMS0uODQtLjg0VjMwLjQzYzAtMi42NS0uNC01LTMuNjgtNS0zLjU1LDAtNi4zNywyLjkyLTYuMzcsN3Y3LjNhLjc2Ljc2LDAsMCwxLS44NC44NGgtLjY0YS43My43MywwLDAsMS0uOC0uODRaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMSAtMC43MSkiIGZpbGw9IiM2ZTZmNzEiLz48cGF0aCBkPSJNMjE4Ljc1LDIzLjI5YzQuNDksMCw3LDMuMjUsNyw4YS44NC44NCwwLDAsMS0uODcuODRIMjEyLjc5Yy4xLDQuMjksMy4wNSw2Ljc0LDYuNTMsNi43NGE3LjIsNy4yLDAsMCwwLDQuNDMtMS41NS42OS42OSwwLDAsMSwxLjEuMmwuMjcuNDFhLjc4Ljc4LDAsMCwxLS4yMywxLjFBOS41Nyw5LjU3LDAsMCwxLDIxOS4yNiw0MWE4LjUyLDguNTIsMCwwLDEtOC44Mi04LjgxQzIxMC40NCwyNi42MSwyMTQuMTksMjMuMjksMjE4Ljc1LDIzLjI5Wm00LjczLDcuMTdjLS4xMy0zLjU1LTIuMjgtNS4zLTQuOC01LjNhNS44LDUuOCwwLDAsMC01Ljc5LDUuM1oiIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0xIC0wLjcxKSIgZmlsbD0iIzZlNmY3MSIvPjxwYXRoIGQ9Ik0yMzcuMTIsMzAuMjNoMXYtLjU0YzAtMy4yNS0xLjc4LTQuMzYtNC4xNi00LjM2YTcuODUsNy44NSwwLDAsMC00LjA4LDEuMTguOC44LDAsMCwxLTEuMTQtLjI3bC0uMi0uMzRhLjc2Ljc2LDAsMCwxLC4yMy0xLjE0LDEwLjM0LDEwLjM0LDAsMCwxLDUuMzYtMS40N2M0LDAsNi4yNywyLjI0LDYuMjcsNi40N3YxMGEuNzQuNzQsMCwwLDEtLjgxLjg0SDIzOWEuNzUuNzUsMCwwLDEtLjg0LS44NFYzOC4zN2E3LjE0LDcuMTQsMCwwLDEsLjEtMS4yN2gtLjA3QTYuMjUsNi4yNSwwLDAsMSwyMzIuNTMsNDFjLTIuODUsMC01LjctMS42Ny01LjctNC45MkMyMjYuODMsMzAuNTMsMjMzLjg3LDMwLjIzLDIzNy4xMiwzMC4yM1pNMjMyLjkzLDM5YzMuMjUsMCw1LjE2LTMuMzUsNS4xNi02LjN2LS44aC0uOTRjLTIuNjUsMC04LC4xLTgsMy44OEMyMjkuMTcsMzcuNCwyMzAuNDEsMzksMjMyLjkzLDM5WiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTEgLTAuNzEpIiBmaWxsPSIjNmU2ZjcxIi8+PHBhdGggZD0iTTI0My42NSwyNC41M2EuNzQuNzQsMCwwLDEsLjgxLS44NEgyNDVhLjcyLjcyLDAsMCwxLC44MS43N3YxLjIxYTYsNiwwLDAsMS0uMSwxLjE0aC4wNmE2LjI4LDYuMjgsMCwwLDEsNS45LTMuNTJjNC41MywwLDcuMzQsMy42Miw3LjM0LDguODVTMjU1LjgyLDQxLDI1MS40Myw0MWE2LjEzLDYuMTMsMCwwLDEtNS41Ny0zLjQyaC0uMDZhNy44NCw3Ljg0LDAsMCwxLC4xMywxLjQ4djcuNGEuNzYuNzYsMCwwLDEtLjg0Ljg0aC0uNjNhLjc0Ljc0LDAsMCwxLS44MS0uODRabTcuNTQsMTQuMzhjMywwLDUuNDctMi40OCw1LjQ3LTYuNzcsMC00LjEzLTIuMjItNi43Ny01LjMzLTYuNzctMi44MiwwLTUuNDcsMi01LjQ3LDYuOEMyNDUuODYsMzUuNTUsMjQ3Ljc0LDM4LjkxLDI1MS4xOSwzOC45MVoiIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0xIC0wLjcxKSIgZmlsbD0iIzZlNmY3MSIvPjwvc3ZnPgo="
            alt="Namecheap"
            class="h-1/3"
          />
        </a>
      </div>
      <div class="flex p-2 px-8 bg-white rounded-lg text-sm h-24">
        <a
          :href="
            'https://www.yay.com/domain-names/?search=' +
            this.$route.query.search
          "
          class="w-full h-full justify-center items-center flex"
        >
          <img
            src="https://www.yay.com/static/img/yay/yay-logo.svg"
            alt="Yay"
            class="h-1/3"
          />
        </a>
      </div>
      <div class="flex p-2 px-8 bg-white rounded-lg text-sm h-24">
        <a
          :href="
            'https://dash.cloudflare.com/?to=/:account/domains/register/' +
            this.$route.query.search +
            '/registration'
          "
          class="w-full h-full justify-center items-center flex"
        >
          <svg
            version="1.1"
            id="Layer_1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            viewBox="0 0 874.3 393.7"
            style="enable-background: new 0 0 874.3 393.7"
            xml:space="preserve"
            class="h-2/3"
          >
            <g>
              <path
                class="st0"
                d="M790.6,271.9c-3.4,0-6.1-2.7-6.1-6.1c0-3.3,2.7-6.1,6.1-6.1c3.3,0,6.1,2.7,6.1,6.1
		C796.7,269.1,793.9,271.9,790.6,271.9 M790.6,260.9c-2.7,0-4.9,2.2-4.9,4.9c0,2.7,2.2,4.9,4.9,4.9c2.7,0,4.9-2.2,4.9-4.9
		C795.5,263.1,793.3,260.9,790.6,260.9 M793.7,269h-1.4l-1.2-2.3h-1.6v2.3h-1.3v-6.7h3.2c1.4,0,2.3,0.9,2.3,2.2c0,1-0.6,1.7-1.4,2
		L793.7,269z M791.3,265.5c0.5,0,1-0.3,1-1c0-0.8-0.4-1-1-1h-2v2L791.3,265.5L791.3,265.5z"
              />
              <polygon
                class="st0"
                points="155.1,259.1 170.7,259.1 170.7,301.6 197.8,301.6 197.8,315.2 155.1,315.2 	"
              />
              <path
                class="st0"
                d="M213.9,287.3v-0.2c0-16.1,13-29.2,30.3-29.2s30.1,12.9,30.1,29v0.2c0,16.1-13,29.2-30.3,29.2
		C226.7,316.3,213.9,303.4,213.9,287.3 M258.5,287.3v-0.2c0-8.1-5.8-15.1-14.4-15.1c-8.5,0-14.2,6.9-14.2,15v0.2
		c0,8.1,5.8,15.1,14.3,15.1C252.8,302.3,258.5,295.4,258.5,287.3"
              />
              <path
                class="st0"
                d="M293.4,290.6v-31.5h15.8v31.2c0,8.1,4.1,11.9,10.3,11.9s10.3-3.7,10.3-11.5v-31.6h15.8v31.1
		c0,18.1-10.3,26-26.3,26C303.4,316.2,293.4,308.2,293.4,290.6"
              />
              <path
                class="st0"
                d="M369.4,259.1H391c20,0,31.7,11.5,31.7,27.7v0.2c0,16.2-11.8,28.2-32,28.2h-21.3L369.4,259.1L369.4,259.1z
		 M391.3,301.4c9.3,0,15.5-5.1,15.5-14.2v-0.2c0-9-6.2-14.2-15.5-14.2H385v28.5H391.3z"
              />
              <polygon
                class="st0"
                points="445.3,259.1 490.2,259.1 490.2,272.7 460.8,272.7 460.8,282.3 487.4,282.3 487.4,295.2 460.8,295.2 
		460.8,315.2 445.3,315.2 	"
              />
              <polygon
                class="st0"
                points="511.8,259.1 527.3,259.1 527.3,301.6 554.5,301.6 554.5,315.2 511.8,315.2 	"
              />
              <path
                class="st0"
                d="M595.1,258.7h15l23.9,56.5h-16.7l-4.1-10h-21.6l-4,10h-16.3L595.1,258.7z M608.8,293.1l-6.2-15.9l-6.3,15.9
		H608.8z"
              />
              <path
                class="st0"
                d="M654,259.1h26.5c8.6,0,14.5,2.2,18.3,6.1c3.3,3.2,5,7.5,5,13.1v0.2c0,8.6-4.6,14.3-11.5,17.2l13.4,19.6h-18
		l-11.3-17h-6.8v17H654L654,259.1L654,259.1z M679.8,286c5.3,0,8.3-2.6,8.3-6.6v-0.2c0-4.4-3.2-6.6-8.4-6.6h-10.2V286L679.8,286
		L679.8,286z"
              />
              <polygon
                class="st0"
                points="726.2,259.1 771.3,259.1 771.3,272.3 741.6,272.3 741.6,280.8 768.5,280.8 768.5,293.1 741.6,293.1 
		741.6,302 771.7,302 771.7,315.2 726.2,315.2 	"
              />
              <path
                class="st0"
                d="M121.1,293.9c-2.2,4.9-6.8,8.4-12.8,8.4c-8.5,0-14.3-7.1-14.3-15.1V287c0-8.1,5.7-15,14.2-15
		c6.4,0,11.3,3.9,13.3,9.3h16.4c-2.6-13.4-14.4-23.3-29.6-23.3c-17.3,0-30.3,13.1-30.3,29.2v0.2c0,16.1,12.8,29,30.1,29
		c14.8,0,26.4-9.6,29.4-22.4L121.1,293.9L121.1,293.9z"
              />
              <g>
                <polygon
                  class="st1"
                  points="752.9,169.6 710,145 702.6,141.8 527.1,143 527.1,232.1 752.9,232.1 		"
                />
                <path
                  class="st2"
                  d="M674.8,223.9c2.1-7.2,1.3-13.8-2.2-18.7c-3.2-4.5-8.6-7.1-15.1-7.4l-123.1-1.6c-0.8,0-1.5-0.4-1.9-1
			c-0.4-0.6-0.5-1.4-0.3-2.2c0.4-1.2,1.6-2.1,2.9-2.2l124.2-1.6c14.7-0.7,30.7-12.6,36.3-27.2l7.1-18.5c0.3-0.8,0.4-1.6,0.2-2.4
			c-8-36.2-40.3-63.2-78.9-63.2c-35.6,0-65.8,23-76.6,54.9c-7-5.2-15.9-8-25.5-7.1c-17.1,1.7-30.8,15.4-32.5,32.5
			c-0.4,4.4-0.1,8.7,0.9,12.7c-27.9,0.8-50.2,23.6-50.2,51.7c0,2.5,0.2,5,0.5,7.5c0.2,1.2,1.2,2.1,2.4,2.1l227.2,0
			c1.3,0,2.5-0.9,2.9-2.2L674.8,223.9z"
                />
                <path
                  class="st3"
                  d="M714,144.8c-1.1,0-2.3,0-3.4,0.1c-0.8,0-1.5,0.6-1.8,1.4l-4.8,16.7c-2.1,7.2-1.3,13.8,2.2,18.7
			c3.2,4.5,8.6,7.1,15.1,7.4l26.2,1.6c0.8,0,1.5,0.4,1.9,1c0.4,0.6,0.5,1.5,0.3,2.2c-0.4,1.2-1.6,2.1-2.9,2.2l-27.3,1.6
			c-14.8,0.7-30.7,12.6-36.3,27.2l-2,5.1c-0.4,1,0.3,2,1.4,2h93.8c1.1,0,2.1-0.7,2.4-1.8c1.6-5.8,2.5-11.9,2.5-18.2
			C781.3,175,751.1,144.8,714,144.8"
                />
              </g>
            </g>
          </svg>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>
