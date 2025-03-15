<template>
  <section class="p-4 grid xs:grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6" >
    <div>
      <VerticalNavigation />
    </div>
    <div>
      <h1 class="min-w-30 inline m-2 p-2 xl:text-2xl sm:text-md xs:text-xs font-bold">
        Services offered
      </h1>
      <p>· Full Stack Development from scratch</p>
      <p>· e-commerce maintanence</p>
      <p>· Web Design</p>
      <p>· SEO</p>
      <p>· Web Accessibility</p>
      <p>· Web Security</p>
      <p>· Web Hosting</p>
      <p>· Web App</p>
    </div>
    <div class="grid justify-end">
      <SlideProjectList />
    </div>   
  </section>
</template>
