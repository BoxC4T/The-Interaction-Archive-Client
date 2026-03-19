<script lang="ts">
    import * as Card from "$lib/components/ui/card/index.js";
   import { Skeleton } from "$lib/components/ui/skeleton/index.js";

</script>
<div class="p-2">
<Card.Root class="w-150 h-75 ">
 <Card.Content class="grid grid-cols-2">
 <!-- Basicly like an id -->
    <div>
        <Skeleton class="h-65 w-50 rounded-xl" />
    </div>
    <div class="space-y-5">
        <Skeleton class="h-4 w-60" />
        <Skeleton class="h-4 w-60" />
        <Skeleton class="h-4 w-60" />
        <Skeleton class="h-4 w-60" />
        <Skeleton class="h-4 w-60" />
        <Skeleton class="h-4 w-60" />
        <Skeleton class="h-4 w-60" />
    </div>
 </Card.Content>
</Card.Root>
</div>