<script>
  import FeedbackList from './components/FeedbackList.svelte'

  let feedback = [
    {
      id: 1,
      rating: 10,
      text: 'in aliquam sem fringilla ut morbi tincidunt augue interdum velit euismod in pellentesque massa placerat duis ultricies lacus sed turpis tincidunt id aliquet risus feugiat',
    },
    {
      id: 2,
      rating: 9,
      text: 'in aliquam sem fringilla ut morbi tincidunt augue interdum velit euismod in pellentesque massa placerat duis ultricies lacus sed turpis tincidunt id aliquet risus feugiat',
    },
    {
      id: 3,
      rating: 8,
      text: 'in aliquam sem fringilla ut morbi tincidunt augue interdum velit euismod in pellentesque massa placerat duis ultricies lacus sed turpis tincidunt id aliquet risus feugiat',
    },
  ]

  function deleteFeedback(event) {
    const itemID = event.detail
    feedback = feedback.filter((fb) => fb.id !== itemID)
  }
</script>

<main class="container">
  <FeedbackList {feedback} on:deletefb={deleteFeedback} />
</main>

<style>
</style>
