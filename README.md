You're looking for the x-cloak directive.

It's a very simple one, it gets removed from the component when Alpine starts up.

So in your case you can add the following style (which will hide elements with the x-cloak attribute) and add x-cloak to your Alpine.js component (in this case the body).

**********************************Code********************************

<style>
  [x-cloak] { display: none }
</style>
<body x-cloak x-data="{openModal: false}" :class="openModal ? 'overflow-hidden' : 'overflow-visible'">

  <button @click="openModal = true">
    Open Modal
  </button>
  <!-- Modal -->
  <div x-show="openModal">
    <!-- content --> 
  </div>
</body>
