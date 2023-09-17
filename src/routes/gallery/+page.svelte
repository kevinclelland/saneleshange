<script lang="ts">

const listData = [
		
        {
            avatar:
                '/images/gallery/25_2.webp',
        },
        {
            avatar:
                '/images/gallery/7_2.webp',
        },
        {
            avatar:
                '/images/gallery/1_2.webp',
        },
        {
			avatar:
				'/images/gallery/9_2.webp',
		},
		{
            avatar:
                '/images/gallery/2_2.webp',
        },
        {
            avatar:
                '/images/gallery/3_2.webp',
        },
        {
            avatar:
                '/images/gallery/4_2.webp',
        },       
        {
            avatar:
                '/images/gallery/10_2.webp',
        },
        {
            avatar:
                '/images/gallery/13_2.webp',
        },
        {
            avatar:
                '/images/gallery/18_2.webp',
        },
        {
            avatar:
                '/images/gallery/34_2.webp',
        },
        {
            avatar:
                '/images/gallery/12_2.webp',
        },
        
        {
            avatar:
                '/images/gallery/14_2.webp',
        },
        {
            avatar:
                '/images/gallery/15_2.webp',
        },
        {
            avatar:
                '/images/gallery/16_2.webp',
        },
        {
            avatar:
                '/images/gallery/17_2.webp',
        },
        
        {
            avatar:
                '/images/gallery/19_2.webp',
        },
        {
            avatar:
                '/images/gallery/21_2.webp',
        },
        {
            avatar:
                '/images/gallery/22_2.webp',
        },
        {
            avatar:
                '/images/gallery/23_2.webp',
        },
        {
            avatar:
                '/images/gallery/24_2.webp',
        },
        {
            avatar:
                '/images/gallery/6_2.webp',
        },
        {
            avatar:
                '/images/gallery/26_2.webp',
        },
        {
            avatar:
                '/images/gallery/27_2.webp',
        },
        {
            avatar:
                '/images/gallery/28_2.webp',
        },
        {
            avatar:
                '/images/gallery/29_2.webp',
        },
        {
            avatar:
                '/images/gallery/30_2.webp',
        },
        {
            avatar:
                '/images/gallery/31_2.webp',
        },
        {
            avatar:
                '/images/gallery/32_2.webp',
        },
        {
            avatar:
                '/images/gallery/35_2.webp',
        },
        {
            avatar:
                '/images/gallery/36_2.webp',
        },
        {
            avatar:
                '/images/gallery/37_2.webp',
        },
        {
            avatar:
                '/images/gallery/38_2.webp',
        },
        {
            avatar:
                '/images/gallery/bike_2.webp',
        },
        {
            avatar:
                '/images/gallery/bikeroth_2.webp',
        },
        {
            avatar:
                '/images/gallery/bob_2.webp',
        },
        {
            avatar:
                '/images/gallery/brad_2.webp',
        },
        {
            avatar:
                '/images/gallery/felix_2.webp',
        },
        {
            avatar:
                '/images/gallery/finish_2.webp',
        },
        {
            avatar:
                '/images/gallery/jan_2.webp',
        },
        {
            avatar:
                '/images/gallery/run1_2.webp',
        },
        {
            avatar:
                '/images/gallery/run2_2.webp',
        },
        {
            avatar:
                '/images/gallery/run3_1.webp',
        },
        {
            avatar:
                '/images/gallery/runroth_1.webp',
        },
        {
            avatar:
                '/images/gallery/swimroth_1.webp',
        },
        {
            avatar:
                '/images/gallery/11_2.webp',
        },
        {
            avatar:
                '/images/gallery/33_2.webp',
        },
        {
            avatar:
                '/images/gallery/8_2.webp',
        },
		
	];

</script>

<h1 class="text-6xl p-4 text-center">Gallery</h1>




<div class="flex flex-wrap grid grid-cols-1 md:grid-cols-4 gap-4 max-w-7xl mx-auto">
    
    <video controls autoplay muted>
        <source src="/images/gallery/vid2.mp4" type="video/mp4">
        
      </video>

        {#each listData as v}
        <div>
            <img class="h-auto max-w-full rounded-lg" src={v.avatar} alt="Sanele in action">
        </div>
        {/each}

</div>
		
	


