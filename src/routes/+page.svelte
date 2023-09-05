<script lang="ts">
	import Card from "$lib/components/card.svelte"
    import portrait from "$lib/assets/images/portraits/portrait.jpg" 
    import Person from '$lib/classes/person'

    let personList: Person[] = [
        new Person(
            "Bluth, George", 
            "george.bluth@reques.in", 
            portrait
        ), 
    ]

</script>

<div class="flex h-screen flex-col gap-5 items-center content-center justify-center p-10 lg:p-20">
    <div class="flex items-center content-center justify-center">
            {#each personList as person, index}
                <Card 
                    avatar="{person.avatar}"
                    id="{(index + 1).toString()}" 
                    name="{person.name}"
                    email="{person.email}"
                />
            {/each}
    </div>

</div>



