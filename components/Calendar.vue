<template>
  <div class="feedback-form">
    <form
      netlify
      netlify-honeypot
      name="feedback"
      method="POST"
      action="/success"
    >
    <p>
     Please submit your request details:
    </p>
      <label for="name">Name</label>
      <input id="name" type="text" name="name" required/>
      <label for="email">Email</label>
      <input id="email" type="email" name="email" required />
      <label for="phone">Phone</label>
      <input id="phone" type="tel" name="phone" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" required />
      <small>Format: 123-456-7890</small>

      
      <label for="meetingtime">Pick a date/time</label>
      <input type="datetime-local" id="meetingtime" name="meetingtime">
          
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<style scoped>
.feedback-form {
  margin: 40px 40px;
  min-width: 250px;
  width: 45%;
}
input,
textarea,
button {
  font-size: inherit;
  margin: 15px 0;
  padding: 12px 20px;
  width: 100%;
}

button {
  background-color: teal;
  border: 1px solid black;
  color: white;
  width: 50%;
}

.hidden {
  clip: rect(0 0 0 0);
  clip-path: inset(50%);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}
</style>
