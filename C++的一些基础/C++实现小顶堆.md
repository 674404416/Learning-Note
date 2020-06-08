# C++实现小顶堆

### 1.实现

```c++
class BinaryHeap {
	//对插入的节点进行上浮,插入是插入在末尾的
	vector<int> upAdjust(vector<int>& nums, int length) {
		//插入的节点和父亲节点
		int child = length - 1;
		int parent = (child - 1) / 2;
		//保存插入的节点
		int temp = nums[child];

		while (child > 0 && nums[parent] > temp) {
		//单向赋值，结束后在正确位置赋值temp
			nums[child] = nums[parent];
			child = parent;
			parent = (child - 1) / 2;
		}
		nums[child] = temp;
		return nums;
	}
	//对删除的节点进行下沉，删除的节点是根节点
	vector<int> downAdjust(vector<int>& nums, int parent, int length) {
		//保存下沉的元素
		int temp = nums[parent];
		//求出下沉元素的子节点
		int child = 2 * parent + 1;

		while (child < length ) {
			if (child + 1 < length && nums[child] > nums[child + 1])
				child++;

			if (nums[child] >= temp)
				break;

			nums[parent] = nums[child];
			parent = child;
			child = 2 * parent + 1;
		}
		nums[parent] = temp;
		return nums;
	}
	vector<int> buildHead(vector<int> nums, int length) {
        //从第一个非叶子节点开始进行下沉
		for (int i = (length - 2) / 2; i >= 0; i--) {
			nums = downAdjust(nums, i, length);
		}
		return nums;
	}
};
```

