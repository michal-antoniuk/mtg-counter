<script>
    export let team;
    export let score;
    export let gameOver;

    function increment() {
        score += 1;
    }

    function decrement() {
        score -= 1;
    }
</script>

<div style="border: dashed {team.toLowerCase()} 5px;" class="col">
    <h2 
        class:text-danger={team === 'Red'}
        class:text-primary={team === 'Blue'}
    >Team {team}: {score}</h2>
    <button disabled={gameOver} on:click={increment} class="btn btn-success">+</button>
    <button disabled={gameOver} on:click={decrement} class="btn btn-danger">-</button>
</div>

<style>
    div.col {
        padding: 20px;
        text-align: center;
    }
</style>