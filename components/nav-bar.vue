<template>
  <div class="navbar bg-base-300 shadow-sm flex justify-between">
    <NuxtLink class="btn btn-ghost normal-case text-xl" to="/">
      Hello
    </NuxtLink>
    <div class="flex-none">
      <ThemeToggle />
      <ul class="menu menu-horizontal px-1">
        <li><a>Link</a></li>
        <li>
          <details>
            <summary>Parent</summary>
            <ul class="bg-base-100 rounded-t-none p-2">
              <li><a>Link 1</a></li>
              <li><a>Link 2</a></li>
            </ul>
          </details>
        </li>
      </ul>
    </div>
  </div>
</template>
