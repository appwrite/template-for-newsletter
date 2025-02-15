<script>
    import { socials } from "$lib/config";
</script>

<footer class="absolute bottom-0 w-full py-5 h-20 border-dashed border-t-2 border-neutral-800 items-center px-5 lg:px-10 text-neutral-secondary font-light">
    <div class="float-left inline-block pb-5">
        <span class="pr-2">Deployed by <a class="text-white underline" href="https://appwrite.io" target="_blank" rel="noopener noreferrer">Appwrite.</a></span>
        <span>Source code on <a class="text-white underline" href="https://github.com/appwrite/template-for-newsletter" target="_blank" rel="noopener noreferrer">Github.</a></span>
    </div>

    <div class="flex gap-3 float-right pb-5">
        {#each socials as social}
            <a class="relative size-8 border rounded-md border-neutral-strong" href={social.url} target="_blank" rel="noopener noreferrer" aria-label={social.name}>
                <object class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-5 h-5 pointer-events-none" title={social.name} type="image/svg+xml" data={`/icons/${social.icon}.svg`}></object>
            </a>
        {/each}
        <a class="relative size-8 border rounded-md border-neutral-strong" href="/admin" aria-label="Admin Panel">
            <object class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-5 h-5 pointer-events-none" title="Admin Panel" type="image/svg+xml" data={`/icons/admin.svg`}></object>
        </a>
    </div>
</footer>