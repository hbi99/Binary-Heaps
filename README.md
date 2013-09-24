Binary-Heaps
============

Very fast alternative to array sort for Javascript

### Simple example
```javascript
// create a heap
var heap = binaryHeap( [10, 3, 4, 8, 2, 9, 7, 1, 2, 6, 5] );

heap.remove(2);
console.log( heap.content );

while (heap.size() > 0) {
	console.log( heap.pop() );
}
```

### A little more advanced example
```javascript
// create a heap with three dimensional array
var heap = binaryHeap([
	[20,0,0],
	[10,10,0],
	[10,10,10],
	[10,0,0],
	[10,0,10]
]);
// returns first from a sorted array
console.log( heap.pop() );
```
