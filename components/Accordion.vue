<template>
    <div class="accordion">
      <div 
        v-for="(item, index) in items" 
        :key="index" 
        class="accordion-item"
        @click="toggleAccordion(index)">
        <div class="accordion-header">
          {{ item.title }}
          <span :class="{'accordion-icon': true, 'minus': activeIndex === index, 'plus': activeIndex !== index}"></span>
        </div>
        <div v-if="activeIndex === index" class="accordion-content">
          {{ item.content }}
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeIndex: null,
        items: [
          { title: 'Post Anything, anytime', content: 'Let’s face it - your grandma knows what this is.  But she isn’t here.  This is the place to do it with the captive audience you’re after.' },
          { title: 'Schedule events', content: 'Set the event, select the guest and send the event, we handle the the rest.    Timers, reminders, notes, video - EDYOU puts it all where you need it.'},
          { title: 'Complete and total security', content: '100% private, encrypted networking.  All users are verified actual college students, faculty and alumni.' },
          { title: 'Created BY students', content: 'Nobody knows what it is to be a student in 2024 without walking in those shoes.  Our team of current and recent graduates know what is needed.' }
        ]
      };
    },
    methods: {
      toggleAccordion(index) {
        this.activeIndex = this.activeIndex === index ? null : index;
      }
    }
  };
  </script>
  
  <style scoped>
  .accordion {
    width: 100%;
    background: none;
  }
  
  .accordion-item {
    border-bottom: 2px solid #000;
    background: none;
    cursor: pointer;
  }
  
  .accordion-header {
    padding: 10px;
  }
  
  .accordion-icon {
    float: right;
    font-size: 1.5em;
    margin-top: -5px;
  }
  
  .minus:before {
    content: "-";
  }
  
  .plus:before {
    content: "+";
  }
  
  .accordion-content {
    padding: 10px;
  }
  </style>
  