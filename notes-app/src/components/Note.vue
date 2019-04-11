<template>
  <div class="ui centered card">
    <!-- <p>Important Tasks: {{ notes.filter(note => {return note.important === true}).length}}</p>
    <p>All Notes: {{notes.filter(note => {return note.important === false}).length}}</p> -->
    <div class="content">
      <div class="header">
        {{ note.title }}
      </div>
      <div class="meta">
        {{ note.project }}
      </div>
      <div class="extra content">
        <span class="right floated edit icon">
          <i class="edit icon"></i>
        </span>
      </div>
    </div>
    <div class="ui bottom attached green basic button" v-show="note.important">
      Important
    </div>
    <div class="ui bottom attached red basic button" v-show="!note.important">
      All Notes
    </div>
    <!-- <note-list v-bind="notes"></note-list> -->
  </div>
</template>

<script type="text/javascript">
    export default {
        props: ["note"],
    };
</script>