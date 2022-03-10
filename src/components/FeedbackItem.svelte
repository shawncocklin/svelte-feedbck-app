<script>
  import { createEventDispatcher } from 'svelte'
  import Card from './Card.svelte'
  export let item

  const dispatch = createEventDispatcher()

  function handleDelete(id) {
    dispatch('deletefb', id)
  }
</script>

<Card>
  <div class="num-display">{item.rating}</div>
  <button class="close" on:click={() => handleDelete(item.id)}>x</button>
  <p class="text-display">{item.text}</p>
</Card>

<style>
  .num-display {
    position: absolute;
    top: -10px;
    left: -10px;
    width: 50px;
    height: 50px;
    background-color: #ff6a95;
    color: #fff;
    border: 1px solid #eee;
    border-radius: 50%;
    padding: 10px;
    text-align: center;
    font-size: 19px;
  }

  .close {
    background: none;
    border: none;
    position: absolute;
    top: 10px;
    right: 20px;
    cursor: pointer;
  }
</style>
