<template>
  <section class="contact-form-section">
    <h2>Contact Me</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name</label>
        <input v-model="form.name" id="name" type="text" required />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input v-model="form.email" id="email" type="email" required />
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea v-model="form.message" id="message" rows="4" required></textarea>
      </div>
      <button type="submit" :disabled="loading">{{ loading ? 'Sending...' : 'Send' }}</button>
      <p v-if="submitted" class="success-msg">Thank you for your message!</p>
      <p v-if="error" class="error-msg">{{ error }}</p>
    </form>
  </section>
</template>

<script setup>
import { reactive, ref } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})
const submitted = ref(false)
const error = ref('')
const loading = ref(false)

async function submitForm() {
  loading.value = true
  error.value = ''
  try {
    const response = await fetch('/api/send-mail', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        name: form.name,
        email: form.email,
        message: form.message
      })
    })
    if (!response.ok) throw new Error('Failed to send message')
    submitted.value = true
    form.name = ''
    form.email = ''
    form.message = ''
    setTimeout(() => { submitted.value = false }, 3000)
  } catch (e) {
    error.value = 'Failed to send message. Please try again later.'
  } finally {
    loading.value = false
  }
}
</script>

<style scoped>
.contact-form-section {
  max-width: 600px;
  margin: 2rem auto;
  padding: 2rem;
  background: #f9f9f9;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.04);
}
.contact-form-section h2 {
  margin-bottom: 1em;
}
.form-group {
  margin-bottom: 1.2em;
}
label {
  display: block;
  margin-bottom: 0.3em;
  font-weight: 500;
}
input, textarea {
  width: 100%;
  padding: 0.6em;
  border: 1px solid #ccc;
  border-radius: 6px;
  font-size: 1em;
}
button {
  background: #42b983;
  color: #fff;
  border: none;
  padding: 0.7em 1.5em;
  border-radius: 6px;
  font-size: 1em;
  cursor: pointer;
  transition: background 0.2s;
}
button:hover {
  background: #369870;
}
.success-msg {
  color: #2ecc71;
  margin-top: 1em;
}
.error-msg {
  color: #e74c3c;
  margin-top: 1em;
}
</style>
