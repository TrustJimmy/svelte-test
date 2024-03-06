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

    <div class="todos">
        {#each todoList as item, index}
            <span class="todo_text">{item.task}</span>
            <div class="todo_buttons"></div>
        {/each}
    </div>
</main>
<h1>My to-do list</h1>
<style>
</style>