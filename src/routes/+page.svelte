<script>
	import { formatList } from '$lib/utils';
</script>

<div class="container mx-auto space-y-4">
	<div class="w-full flex flex-col justify-center items-center">
		<div class="text-center mt-4">
			<div>
				<h1>Welcome to MagiConvert</h1>
				<p class="py-6">your one-stop shop for image conversion and resizing</p>
				<a href="/app" class="btn variant-filled">Get Converting</a>
			</div>
		</div>
	</div>
    <section class="w-full text-center flex flex-col justify-center items-center">
        <h2 class="font-bold text-2xl">Easier Done than Said</h2>
        <div class="">
            <ul class="list">
                <li class=""><span  class="badge-icon p-4 variant-soft-primary">1</span><span class="flex-auto">Select your image</span></li>
                <li class=""><span  class="badge-icon p-4 variant-soft-primary">2</span><span class="flex-auto">Select your format and size</span></li>
                <li class=""><span  class="badge-icon p-4 variant-soft-primary">3</span><span class="flex-auto">Click the button</span></li>
                <li class=""><span  class="badge-icon p-4 variant-soft-primary">4</span><span class="flex-auto">Download your created image</span></li>
            </ul>
        </div>
    </section>
    <section class="w-full text-center mt-5">
        <h2 class="font-bold text-2xl">Supported Formats and Conversions</h2>
        <div class="gap-4 flex justify-evenly items-center flex-wrap">
            {#each formatList as format}
                <a class="w-32 h-32 rounded-full flex justify-center items-center border border-surface-500" href="/app/convert?format={format}">
                    <span>{format}</span>
                </a>
            {/each}
        </div>
    </section>
</div>
