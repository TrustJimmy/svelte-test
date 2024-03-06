<script>
    let newItem="";
    let todoList = [];
    function add() {
        if(newItem !=="") {
            todoList = [
                ...todoList,
                {
                    задача: newItem,
                    завершено:false,
                },
            ];
            newItem="";
        }
    }
</script>
<main>
    <form on:submit={add}>
        <input bind:value={newItem} placeholder="Enter to-do"/>
        <button class="add-todo" on:click={add}><span>+</span></button>
    </form>
</main>
<style>
</style>