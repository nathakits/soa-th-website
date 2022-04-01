<template>
  <div>
    <h1>Journey</h1>
    <form id="journey-form">
      <label>Name</label>
      <input name="name" id="name" />
      <label>Name</label>
      <input id="opinion_agree" type="radio" name="opinion" value="agree" />
      <input
        id="opinion_disagree"
        type="radio"
        name="opinion"
        value="disagree"
      />
      <button onclick="submitForm()">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'JourneyPage',
  methods: {
    submitForm(event) {
      const formData = new FormData(event.target)

      // fields
      const name = document.getElementById('name').val() || 'Not set'
      const opinion = () => {
        let op = ''
        document.querySelectorAll('[name="opinion"]').forEach((el) => {
          if (el.prop('checked') === true) {
            op = el.val()
          }
        })
        return op
      }

      // fetch(
      //   'https://docs.google.com/forms/u/0/d/e/1FAIpQLSehT2PjsjK998bqA-D0uhhng02fjvg-qcFU9RwyRo5BTrAIwg/formResponse',
      //   {
      //     method: 'Post',
      //     body: formData,
      //     mode: 'no-cors',
      //   }
      // )
      //   .then((response) => {
      //     console.log(response)
      //     console.log(`submitted`)
      //   })
      //   .catch((err) => {
      //     console.log('Error', err)
      //   })

      const data = {
        'entry.1687737570': name,
        'entry.2050792409_sentinel': opinion(),
      }
    },
  },
}
</script>


<style>
</style>