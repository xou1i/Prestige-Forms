<script>

// onclick hire me button scroll to contact section
  function scrollToContact() {
    const hireMeButton = document.getElementById('HIRE');
    const contactSection = document.getElementById('contact');
    if (contactSection === hireMeButton) {
      contactSection.scrollIntoView({ behavior: 'smooth' });
    }
  }
</script>