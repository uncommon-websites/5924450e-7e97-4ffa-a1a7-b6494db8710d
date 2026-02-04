<script lang="ts">
    import ProductCard from './ProductCard.svelte';

    const products = [
        {
            badge: "Bestseller",
            code: "Ethiopia",
            title: "Yirgacheffe Natural",
            image: "/generated/image-close-up-of-premium-single-origin-coffee-1770230955906-1.webp", 
            price: "$22"
        },
        {
            badge: "New Arrival",
            code: "Colombia",
            title: "Geisha Auction Lot",
            image: "/generated/image-close-up-of-premium-single-origin-coffee-1770230955906-1.webp", 
            price: "$28"
        },
        {
            badge: "Limited",
            code: "Kenya",
            title: "AA Nyeri Peaberry",
            image: "/generated/image-close-up-of-premium-single-origin-coffee-1770230955906-1.webp",
            price: "$24"
        },
        {
            badge: "Fan Favorite",
            code: "Guatemala",
            title: "Antigua Volcanic",
            image: "/generated/image-close-up-of-premium-single-origin-coffee-1770230955906-1.webp",
            price: "$20"
        }
    ];
</script>

<section class="bg-[oklch(0.473_0.137_46.201)] py-24">
    <div class="container mx-auto px-6 md:px-12">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 text-white">
            <div class="max-w-xl">
                <h2 class="text-4xl md:text-[44px] leading-tight font-medium tracking-tight mb-6">Exceptional coffee starts with exceptional beans.</h2>
                <p class="text-[17px] text-white/80 font-light max-w-md leading-relaxed">Single-origin beans from the world's finest coffee regions, roasted fresh to order in small batches for maximum flavor.</p>
            </div>
            <a href="/" class="hidden md:inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors mt-6 md:mt-0 tracking-wide uppercase">
                Shop All Origins <span class="ml-2">→</span>
            </a>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
            {#each products as product}
                <ProductCard {...product} isDark={true} />
            {/each}
        </div>

        <div class="mt-12 text-center md:hidden">
            <a href="/" class="inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors text-white tracking-wide uppercase">
                Shop All Origins <span class="ml-2">→</span>
            </a>
        </div>
    </div>
</section>
