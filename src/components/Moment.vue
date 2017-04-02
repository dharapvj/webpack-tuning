<template>
  <h1>Moment.format called. Today's date is {{currDate}}</h1>
</template>

<script>
import moment from 'moment';

// moment().format('MMM Do YY');
export default {
  data() {
    return {
      currDate: moment().format('MMM Do, YYYY'),
    };
  },
};
</script>
