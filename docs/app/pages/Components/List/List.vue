<example src="./examples/SingleLine.vue" />
<example src="./examples/DoubleLine.vue" />
<example src="./examples/TripleLine.vue" />
<example src="./examples/ListTypes.vue" />
<example src="./examples/ListExpansion.vue" />
<example src="./examples/Controls.vue" />

<template>
  <page-container centered :title="$t('pages.list.title')">
    <div class="page-container-section">
      <p>Lists present multiple line items vertically as a single continuous element and are best suited for similar data types.</p>
      <p>They can have one, two or three lines of content, with a lot of different contents. Even that the examples on this page may look like that lists can only be used in mobile viewport, you can and should use them in desktop too.</p>
      <p>List items can have interaction events, like click and mousedown events. They also integrate nicely with Vue Router.</p>
    </div>

    <div class="page-container-section">
      <h2>List</h2>

      <p>Single line lists are really great for navigational elements, such as drawers. You can pass a icons, text and actions to them. They have also a dense layout, to accommodate more items on the screen:</p>
      <code-example title="Single Line" :component="examples['single-line']" />
    </div>

    <div class="page-container-section">
      <p>The double line lists are good to show additional information about single items:</p>
      <code-example title="Double Line" :component="examples['double-line']" />
    </div>

    <div class="page-container-section">
      <p>The three line lists are great for showing a preview of the full content of the item. It's good for email lists and other information like that:</p>
      <code-example title="Triple Line" :component="examples['triple-line']" />
    </div>

    <div class="page-container-section">
      <h2>List Actions</h2>

      <p>List items will render different tags based on the interaction types given.</p>
      <p>If you pass one of those event, the item will automatically render a <code>button</code>:</p>
      <ul>
        <li v-for="event in interactionEvents" :key="event">{{ event }}</li>
      </ul>

      <p>If you pass a <code>href</code> attribute, the item will automatically render an <code>a</code> tag.</p>
      <p>All <a href="https://router.vuejs.org/en/api/router-link.html" target="_blank">options</a> of <code>router-link</code> can be simply used here. This will render an <code>a</code> tag:</p>
      <code-example title="Different types" :component="examples['list-types']" />
    </div>

    <div class="page-container-section">
      <p>Lists accept controls as main toggle actions. Really useful to improve form layouts:</p>
      <code-example title="Controls" :component="examples['controls']" />
    </div>

    <div class="page-container-section">
      <p>Lists can have expansion panels to reveal more options:</p>
      <code-example title="Expansion" :component="examples['list-expansion']" />

      <api-item title="API - md-list">
        Coming soon...
      </api-item>
    </div>
  </page-container>
</template>

<script>
  import examples from 'docs-mixins/docsExample'
  import MdInteractionEvents from 'core/utils/MdInteractionEvents'

  export default {
    name: 'DocList',
    mixins: [examples],
    data: () => ({
      interactionEvents: MdInteractionEvents
    })
  }
</script>
