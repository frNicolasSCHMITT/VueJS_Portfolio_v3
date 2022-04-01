<script>
export default {
  data() {
    return {
      name: '',
      contact: '',
      purpose: '',
      message: '',
    }
  }
}
</script>

<template>
  <h1>Contact Me</h1>
  <section class="contact-section">
    <form action="Form.php" method="post">
      <div class="input-group">
        <label for="name">Name / Designation</label>
        <input v-model="name" placeholder="Who are you ?">
        <p>
          {{name}}
        </p>
      </div>
      <div class="input-group">
        <label for="contact">Contact Information</label>
        <input v-model="contact" placeholder="How to contact you back ?">
        <p>
          {{contact}}
        </p>
      </div>
      <div class="input-group">
        <label for="purpose">Message Purpose</label>
        <select v-model="purpose">
          <option disabled value=""> What is the purpose of your message ?</option>
          <option>Business opportunity</option>
          <option>Recruitment proposal</option>
          <option>Other purposes</option>
        </select>
        <p>
          {{purpose}}
        </p>
      </div>
      <div class="input-group">
        <label for="message">Message Content</label>
        <textarea v-model="message" placeholder="What is your message for me ?"></textarea>
        <p>
          {{message}}
        </p>
      </div>
      <input class="form-submit" type="submit" value="Send">
    </form>
  </section>
</template>

<style scoped>

.contact-section{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contact-section form{
  display: flex;
  flex-direction: column;
  text-align: center;
  width: 90%;
  margin: 0 5%;
  max-width: 500px;
}

.input-group{
  display: flex;
  flex-direction: column;
  margin: 20px 0;
}

.input-group label{
  padding: 10px 0;
  font-size: 1.5rem;
  color: rgba(0, 189, 126, 1);
}

.input-group input, select, textarea {
  min-height: 30px;
  border-radius: 10px;
  resize: vertical;
}

.form-submit {
  color: rgba(0, 189, 126, 1);
  font-size: 1.5rem;
  font-weight: bold;
  border-radius: 10px;
  border: solid 3px rgba(0, 189, 126, 1);
  width: 100px;
  margin: 0 calc(50% - 50px);
  cursor: pointer;
}

.form-submit:hover {
  background-color: transparent;
  box-shadow: 0 0 20px rgba(0, 189, 126, 1);
}

</style>
