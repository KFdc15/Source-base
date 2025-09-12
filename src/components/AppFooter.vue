<template>
  <footer class="border-t border-slate-200 bg-white/80 backdrop-blur">
  <div class="mx-auto max-w-7xl px-4 py-2 text-sm flex flex-col md:flex-row items-center gap-2 md:gap-4">
      <!-- Left: Brand -->
      <div class="flex-1 text-center md:text-left text-slate-700">
        <span class="font-semibold text-slate-900">MyLogo</span>
        <span class="ml-2">© {{ new Date().getFullYear() }}. All rights reserved.</span>
      </div>

      <!-- Center: Links -->
      <nav class="hidden md:flex items-center justify-center gap-6 text-sm">
        <a href="#" class="text-slate-600 hover:text-slate-900 transition-colors">Privacy</a>
        <a href="#" class="text-slate-600 hover:text-slate-900 transition-colors">Terms</a>
        <a href="#" class="text-slate-600 hover:text-slate-900 transition-colors">Support</a>
      </nav>

      <!-- Right: Socials -->
      <div class="flex-1 flex justify-center md:justify-end gap-3">
        <a href="#" aria-label="Twitter" class="text-slate-500 hover:text-slate-800">
          <svg class="h-4 w-4" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path d="M22 5.8c-.7.3-1.4.5-2.2.6.8-.5 1.4-1.3 1.7-2.2-.8.5-1.7.9-2.6 1.1A3.7 3.7 0 0 0 12 7.3c0 .3 0 .6.1.9-3.1-.2-5.9-1.7-7.8-4-.3.6-.5 1.3-.5 2 0 1.3.7 2.5 1.7 3.2-.6 0-1.2-.2-1.7-.5v.1c0 1.8 1.3 3.3 3 3.6-.3.1-.6.1-.9.1-.2 0-.4 0-.6-.1.4 1.4 1.8 2.4 3.4 2.4A7.4 7.4 0 0 1 2 18.4c1.6 1 3.5 1.6 5.5 1.6 6.6 0 10.3-5.5 10.3-10.3v-.5c.7-.4 1.3-1.1 1.8-1.8z"/>
          </svg>
        </a>
        <a href="#" aria-label="GitHub" class="text-slate-500 hover:text-slate-800">
          <svg class="h-4 w-4" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path fill-rule="evenodd" d="M12 2C6.5 2 2 6.6 2 12.2c0 4.5 2.9 8.3 6.9 9.7.5.1.7-.2.7-.5v-1.8c-2.8.6-3.4-1.2-3.4-1.2-.4-1-1-1.3-1-1.3-.8-.6.1-.6.1-.6.9.1 1.4 1 1.4 1 .8 1.4 2.1 1 2.6.8.1-.6.3-1 .6-1.3-2.2-.3-4.5-1.1-4.5-5 0-1.1.4-2 .9-2.7-.1-.3-.4-1.3.1-2.6 0 0 .8-.3 2.7 1 .8-.2 1.6-.3 2.4-.3s1.6.1 2.4.3c1.9-1.3 2.7-1 2.7-1 .5 1.3.2 2.3.1 2.6.6.7.9 1.6.9 2.7 0 3.9-2.3 4.7-4.5 5 .3.3.6.8.6 1.6v2.4c0 .3.2.6.7.5A10.2 10.2 0 0 0 22 12.2C22 6.6 17.5 2 12 2z" clip-rule="evenodd"/>
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>

