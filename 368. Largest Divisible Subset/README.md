# 368. Largest Divisible Subset

找一个序列中满足整除关系的最大子集，这样的子集满足一个性质：
> 能加入一个这种子集的数，要么被子集中的最大数整除，要么整除子集中的最小数

将序列排序，这样只要从前往后判断整除关系即可

每个数组元素x对应一个集合set，包含了以x为最大值的整除关系最大子集。因此根据上述性质，新数遍历前面的元素，如能整除，则这个元素对应的子集加入候选集。最后取长度最大的一个子集，加上这个新数自身，作为这个新数的子集

遍历完成后，取子集中长度最大的，即为题求的序列