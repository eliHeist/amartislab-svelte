

<script>
import MoreBtn from "../moreBtn.svelte";
import ProjectCard from "./projectCard.svelte";

export let projects
</script>

<section id="featured-projects">
    <div class="container">
        <div class="py-3">
            <h4 class="display-5 text-center text-white py-5">Our Work</h4>
          </div>
        <div class="row">
            {#each projects as project}
            <div class="col col-4">
                <ProjectCard title="{project.name}" img={project.thumbnail}/>
            </div>
            {/each}
        </div>
        <div class="mt-5 d-flex">
            <MoreBtn text="Explore more" link="#" classes="ms-auto" />
          </div>
    </div>
</section>

<style></style>