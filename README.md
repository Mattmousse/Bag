# Bag

 * This interface represents a collection of integers, similar to a set but allowing duplicates.
 * The collection is iterable and provides basic operations like adding, removing,
 * and counting elements.
 *
 * Here is an example of how to use a Bag:
 *
 *         Bag b = create();
 *         b.add(4);
 *         b.add(8);
 *         b.add(4);
 *         b.add(2);
 *         // at this point the content of the bag is {4, 8, 4, 2} (the order is not important)
 *         b.count(4); // returns 2 since there are two occurrences of 4 in the bag
 *         b.count(1); // returns 0 since there are no occurrences of 1 in the bag
 *         b.count(8); // returns 1 since there is one occurrence of 8 in the bag
 *         b.remove(4);
 *         // at this point the content of the bag is {4, 8, 2}
 *         b.count(4); // returns 1 since there is one occurrence of 4 in the bag
 *         b = b.filter(x -> x >= 4); // returns a new Bag containing 4, 8 since only those elements are >= 4
 *         // at this point the content of the bag is {4, 8}
 *         b.count(2); // returns 0 since there are no occurrences of 2 in the bag
 *         // iterate over the elements of the bag. This implicitly uses the iterator() method
 *         for (int i : b) { // prints 4, 8 (in any order)
 *             System.out.println(i);
 *         }
