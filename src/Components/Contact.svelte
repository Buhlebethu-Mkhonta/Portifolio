<script>
  import { onMount } from 'svelte';

  let formData = {
    name: '',
    email: '',
    subject: '',
    message: ''
  };

  let errors = {
    email: ''
  };

  let isSubmitting = false;
  let submitStatus = '';

  onMount(() => {
    formData = {
      name: '',
      email: '',
      subject: '',
      message: ''
    };
    submitStatus = '';
  });

  function validateEmail(email) {
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return emailRegex.test(email);
  }

  function handleSubmit(event) {
    event.preventDefault();
    isSubmitting = true;
    submitStatus = '';
    errors.email = '';

    if (!validateEmail(formData.email)) {
      errors.email = 'Please enter a valid email address';
      isSubmitting = false;
      return;
    }

    // Reset form
    formData = {
      name: '',
      email: '',
      subject: '',
      message: ''
    };
    submitStatus = 'success';
    isSubmitting = false;
  }
</script>


<section id="contact" class="bg-[#181c23] py-16 px-2 sm:px-4 w-full">
    <div class="text-center mt-8 mb-10">
        <h2 class="text-3xl md:text-4xl font-extrabold text-white mb-2">Get In <span class="text-red-500">Touch</span></h2>
        <p class="text-[#b0b8c1] max-w-2xl mx-auto text-base md:text-lg">
          Interested in working together? Have questions about my services? Feel free to reach out and I'll get back to you as soon as possible.
        </p>
    </div>
  <div class="max-w-6xl mx-auto flex flex-col md:flex-row gap-10">
    <!-- Contact Info Card -->
    <div class="flex-1 bg-[#23272f] rounded-2xl shadow-lg p-8 flex flex-col justify-between min-w-[300px]">
      <div>
        <h3 class="font-semibold text-white text-lg mb-6">Contact Information</h3>
        <ul class="space-y-6 mb-8">
          <li class="flex items-center gap-4">
            <span class=" text-white rounded-full p-3 text-xl"><i class='bx bx-envelope'></i></span>
            <div>
              <div class="font-bold text-white text-sm">Email</div>
              <div class="text-[#b0b8c1] text-sm">buhlebethumkhonta@gmail.com</div>
            </div>
          </li>
          <li class="flex items-center gap-4">
            <span class=" text-white rounded-full p-3 text-xl"><i class='bx bx-phone'></i></span>
            <div>
              <div class="font-bold text-white text-sm">Phone</div>
              <div class="text-[#b0b8c1] text-sm">+268 76876243</div>
            </div>
          </li>
          <li class="flex items-center gap-4">
            <span class=" text-white rounded-full p-3 text-xl"><i class='bx bx-map'></i></span>
            <div>
              <div class="font-bold text-white text-sm">Location</div>
              <div class="text-[#b0b8c1] text-sm">Eswatini, Southern Africa</div>
            </div>
          </li>
        </ul>
        <div>
          <div class="font-semibold text-white mb-2">Connect With Me</div>
          <div class="flex gap-4">
            <a href="https://www.linkedin.com/in/buhlebethu-mkhonta" aria-label="LinkedIn" class="bg-[#181c23] hover:bg-red-500 text-white rounded-md p-2 transition" target="_blank"><i class='bx bxl-linkedin'></i></a>
            <a href="https://github.com/percy-san" aria-label="GitHub" class="bg-[#181c23] hover:bg-red-500 text-white rounded-md p-2 transition" target="_blank"><i class='bx bxl-github'></i></a>
          </div>
        </div>
      </div>
    </div>
    <!-- Contact Form -->
    <div class="flex-1 bg-[#23272f] rounded-2xl shadow-lg p-8">
      <h3 class="font-semibold text-white text-lg mb-6">Send Me a Message</h3>
      <form class="space-y-4" on:submit|preventDefault={handleSubmit}>
        <div class="flex flex-col md:flex-row gap-4">
          <div class="w-full">
            <label for="name" class="block text-white text-sm font-medium mb-2">Your Name</label>
            <input 
              type="text" 
              id="name"
              bind:value={formData.name}
              class="input input-bordered w-full bg-[#181c23] text-white border-[#23272f] focus:border-red-500" 
              required
            />
          </div>
          <div class="w-full">
            <label for="email" class="block text-white text-sm font-medium mb-2">Your Email</label>
            <input 
              type="email" 
              id="email"
              bind:value={formData.email}
              class="input input-bordered w-full bg-[#181c23] text-white border-[#23272f] focus:border-red-500" 
              required
            />
            {#if errors.email}
              <p class="text-red-500 text-sm mt-1">{errors.email}</p>
            {/if}
          </div>
        </div>
        <div>
          <label for="subject" class="block text-white text-sm font-medium mb-2">Subject</label>
          <input 
            type="text" 
            id="subject"
            bind:value={formData.subject}
            class="input input-bordered w-full bg-[#181c23] text-white border-[#23272f] focus:border-red-500" 
            required
          />
        </div>
        <div>
          <label for="message" class="block text-white text-sm font-medium mb-2">Your Message</label>
          <textarea 
            id="message"
            bind:value={formData.message}
            class="textarea textarea-bordered w-full min-h-[120px] bg-[#181c23] text-white border-[#23272f] focus:border-red-500"
            required
          ></textarea>
        </div>
        <button 
          type="submit" 
          class="btn bg-red-500 border-none hover:bg-red-600 text-white w-full mt-2"
          disabled={isSubmitting}
        >
          {#if isSubmitting}
            Sending...
          {:else}
            Send Message
          {/if}
        </button>

        {#if submitStatus === 'success'}
          <p class="text-green-500 text-center mt-2">Message sent successfully!</p>
        {:else if submitStatus === 'error'}
          <p class="text-red-500 text-center mt-2">Failed to send message. Please try again.</p>
        {/if}
      </form>
    </div>
  </div>
</section>
