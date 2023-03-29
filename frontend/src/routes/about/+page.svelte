<script>
    import { Heading, AccordionItem, Accordion } from "flowbite-svelte";
</script>

<Heading
    tag="h2"
    customSize="text-4xl font-extrabold mx-10 mt-5"
    class="font-mono">Calculator</Heading
>
<Heading tag="h4" customSize="text-2xl mx-10 mt-5 mb-5" class="font-mono"
    >Calculator for Division</Heading
>

<div class="mx-10 pb-5">
    <Accordion>
        <AccordionItem open>
            <span slot="header" class="font-mono">What is this site for?</span>
            <p class="font-mono">
                This is an online calculator for division only. On the main
                page, enter the dividend in the num1 field and the divisor in
                the num2 field. After that, press the calculate button to return
                the quotient.
            </p>
        </AccordionItem>
        <AccordionItem open>
            <span slot="header" class="font-mono">Is this site all built?</span>
            <p class="font-mono">Not yet!</p>
        </AccordionItem>
    </Accordion>
</div>
