<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<div class="fixed w-full z-50 transition-colors duration-300 top-0 left-0 font-sans" class:text-white={!isScrolled} class:text-gray-900={isScrolled}>
  <!-- Top Bar -->
  <div class="bg-gradient-to-r from-[oklch(0.879_0.169_91.605)] to-[oklch(0.828_0.189_84.429)] text-[11px] font-medium tracking-wide text-center py-2.5 flex justify-center items-center gap-1 cursor-pointer hover:underline text-gray-900">
    <span>Freshly Roasted to Order — Free Shipping on Orders $40+</span>
    <span class="text-[10px]">➜</span>
  </div>

  <!-- Main Nav -->
  <nav class="flex justify-between items-center px-6 py-4 md:px-10 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-3 text-gray-900' : 'bg-transparent text-white'}">
    <!-- Left Links -->
    <div class="hidden md:flex items-center gap-8 text-[13px] font-medium tracking-wide">
      <a href="/" class="hover:opacity-60 transition-opacity">Shop</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Our Story</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Brewing Guide</a>
    </div>

    <!-- Logo -->
    <div class="absolute left-1/2 transform -translate-x-1/2">
      <a href="/" class="block flex items-center gap-2">
        <svg class="w-8 h-8" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <mask
            id="mask0_161_7365"
            style="mask-type:luminance"
            maskUnits="userSpaceOnUse"
            x="3"
            y="1"
            width="18"
            height="22"
          >
            <path d="M3 1H20.7794V22.3353H3V1Z" fill="white" />
          </mask>
          <g mask="url(#mask0_161_7365)">
            <path
              d="M14.1516 3.24638L12.4034 2.77795L10.9302 8.27606L9.60014 3.31233L7.85194 3.78076L9.28896 9.14369L5.70969 5.56443L4.42993 6.84419L8.35594 10.7702L3.46671 9.46017L2.99829 11.2083L8.34038 12.6397C8.27922 12.3759 8.24687 12.1011 8.24687 11.8187C8.24687 9.81953 9.86746 8.19894 11.8666 8.19894C13.8657 8.19894 15.4863 9.81953 15.4863 11.8187C15.4863 12.0993 15.4544 12.3724 15.394 12.6347L20.2489 13.9356L20.7173 12.1874L15.354 10.7503L20.2436 9.44012L19.7751 7.69196L14.412 9.12898L17.9913 5.54972L16.7115 4.26998L12.84 8.14156L14.1516 3.24638Z"
              fill="currentColor"
            />
            <path
              d="M15.3888 12.655C15.2389 13.2887 14.9225 13.8579 14.4883 14.314L18.0056 17.8313L19.2853 16.5515L15.3888 12.655Z"
              fill="currentColor"
            />
            <path
              d="M14.4529 14.3508C14.0135 14.7996 13.4582 15.1345 12.8354 15.3071L14.1153 20.0836L15.8635 19.6151L14.4529 14.3508Z"
              fill="currentColor"
            />
            <path
              d="M12.7701 15.3246C12.4812 15.3989 12.1784 15.4384 11.8663 15.4384C11.5319 15.4384 11.2082 15.393 10.9008 15.3082L9.61981 20.089L11.368 20.5574L12.7701 15.3246Z"
              fill="currentColor"
            />
            <path
              d="M10.839 15.2905C10.2258 15.1093 9.68038 14.7702 9.24994 14.3201L5.72406 17.8459L7.00382 19.1257L10.839 15.2905Z"
              fill="currentColor"
            />
            <path
              d="M9.22084 14.2889C8.79778 13.836 8.48962 13.2743 8.34294 12.6505L3.47211 13.9556L3.94053 15.7038L9.22084 14.2889Z"
              fill="currentColor"
            />
          </g>
        </svg>
        <span class="text-xl font-bold tracking-tight">My Friend's Coffee</span>
      </a>
    </div>

    <!-- Right Links -->
    <div class="flex items-center gap-6 md:gap-8">
      <a href="/" class="text-[13px] font-medium tracking-wide hover:opacity-60 transition-opacity hidden md:block">Account</a>
      <a href="/" class="{isScrolled ? 'bg-[oklch(0.555_0.163_48.998)] text-white' : 'bg-white text-gray-900'} px-5 py-2 rounded-full text-[13px] font-bold tracking-wide hover:opacity-90 transition-all shadow-sm">Shop Coffee</a>
      <button class="md:hidden">
        <!-- Mobile Menu Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </div>
  </nav>
</div>
