<template>
    <div class="bg-slate-100 p-4 relative">
        <div class="container mx-auto flex items-center justify-between gap-4">
            <div>
                <a href="/">LOGO</a>
            </div>
            <div>
                <ul class="absolute left-0 top-full bg-slate-300 w-full h-[100vh]">
                    <li class="py-2 text-center" v-for="link in links"><a :href="link.path">{{ link.name }}</a></li>
                </ul>
            </div>
            <div>
                <p>Profile Picture</p>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    setup() {
        const links =
            [
                { id: 1, path: '/', name: 'Home' },
                { id: 2, path: '/about', name: 'About' },
                { id: 3, path: '/contact', name: 'Contact' },
                { id: 4, path: '/shop', name: 'Shop' },
                { id: 5, path: '/gallery', name: 'Gallery' },
            ]

        return { links }
    }
}
</script>