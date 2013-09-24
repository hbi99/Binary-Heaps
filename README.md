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

### Benchmark 1 - 1.000.000 integers in array
```javascript
var arr = [],
	heap = binaryHeap(),
	start_time,
	el,
	i=0,
	il=1000000;

for (; i<il; i++) {
	el = Math.ceil(Math.random() * il)+1;
	arr.push( el );
	heap.push( el );
}

// Benchmark: Javascript built-in sort-method
start_time = Date.now();
arr.sort(function(a,b){return a - b});
console.log( 'Lowest element in array using JS sort: '+ arr[0] +' ('+ ( Date.now() - start_time ) +'ms)');
// ~158ms

// Benchmark: Binary Heap
start_time = Date.now();
console.log( 'Lowest element in array using Binary Heap: '+ heap.pop() +' ('+ ( Date.now() - start_time ) +'ms)');
// ~1ms
```



