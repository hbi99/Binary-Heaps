Binary-Heaps
============

Very fast alternative to array sort for Javascript

## Sample Usage

```html
<script type='text/javascript' src='binary_heap.js'></script>
<script type='text/javascript'>
  // create a heap
  var heap = binaryHeap( [10, 3, 4, 8, 2, 9, 7, 1, 2, 6, 5] );
  
  heap.remove(2);
  console.log( heap.content );
  
  while (heap.size() > 0) {
  	console.log( heap.pop() );
  }
</script>```
