<script>
    import { Input, Label, Helper } from "flowbite-svelte";
    import { Button } from "flowbite-svelte";
    import { Heading, P, A, Mark, Secondary } from "flowbite-svelte";
</script>

<Heading tag="h2" customSize="text-4xl font-extrabold mx-10 mt-5"
    >Calculator</Heading
>
<Heading tag="h4" customSize="text-3xl font-light mx-10">Calculator</Heading>
<P class="my-4 text-gray-500 mx-10 my-2">Calculator for division</P>

<div class="rounded-lg border mx-10 my-5 px-10 py-5">
    <div class="mb-6">
        <div>
            <Label for="num1" class="mb-2">Number 1</Label>
            <Input type="number" id="num1" placeholder="dividened" required />
        </div>
        <div>
            <Label for="num2" class="mb-2">Number 2</Label>
            <Input type="number" id="num2" placeholder="division" required />
        </div>
        <div class="text-center">
            <Button class="m-5 ">Calculate</Button>
        </div>
    </div>
</div>
