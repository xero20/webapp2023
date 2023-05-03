<script>
    export let data;
    import { P, Spinner } from "flowbite-svelte";
    import { get } from "$lib/utils.js";
    import { onMount } from "svelte";

    let result;
    //let loaded=false;
    async function get_result() {
        result = await get(`/result?task_id=${data.task_id}`);
        // if running: 1000ms 뒤에 다시 get result, if finished:
        // svelt에서 #if
        if (result.status == "running") {
            setTimeout(get_result, 1000);
        } //else {
        //loaded = true;
        //}
    }

    //onMount - HTML 로딩 -> onMount -> get_result   익명함수에 인자로 함수를 넣어줌.
    onMount(async () => {
        get_result();
    });

    //    function a() {
    //       console.log('a');
    //  }

    //  let b=() => {

    //}
</script>

{#if result}
    <P>Task ID: {result.task_id}</P>
    <P>Status: {result.status}</P>
    {#if result.status == "running"}
        <P>Result: <Spinner size={4} /></P>
    {:else}
        <P>Result: {result.result}</P>
    {/if}
{/if}
