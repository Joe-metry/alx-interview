							Project Overview:
							-----------------


To implement the canUnlockAll function in Python:

Initialize a boolean list called visited to keep track of whether each box has been visited or not. Initially, set all elements of visited to False.

Mark the first box (index 0) as visited since it's unlocked.

Create a list called keys and add the keys from the first box (boxes[0]) to it.

Start a while loop until there are no more keys in the keys list:

Pop a key from the keys list.
If the key corresponds to a locked box (i.e., the box is not yet visited), mark the box as visited, and add the keys from that box to the keys list.
After the while loop, check if all boxes have been visited (i.e., if all elements in the visited list are True).

If all boxes have been visited, return True to indicate that all boxes can be opened. Otherwise, return False.
