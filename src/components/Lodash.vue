<template>
<div>
  <h1>Lodash usage demo</h1>
  <p>See how we loaded <code>lodash</code> library and executed it's <code>pick()</code> function</p>
  <div>
    <pre class="code">
let iphone = {
	RAM: '8gb',
	retina: true,
	screen: 'touch',
	'lightning': true
};
let mobile = _.pick(iphone,['RAM', 'screen']);
    </pre>
  </div>
  <div id="lodash">
  Original Object <pre class='code iphone'>{{origObj}}</pre>
  <br>"Pick"ed Object <pre class='code mobile'>{{pickedObj}}</pre>
  </div>
</div>

</template>

<script>
// improvement: load only what you need from lodash.
import pick from 'lodash/pick';

const iphone = {
  RAM: '8gb',
  retina: true,
  screen: 'touch',
  lightning: true,
};
const mobile = pick(iphone, ['RAM', 'screen']);

export default {
  data() {
    return {
      origObj: JSON.stringify(iphone, null, 2),
      pickedObj: JSON.stringify(mobile, null, 2),
    };
  },
};
</script>
