/**
 * Created by Nate He on 4/1/2017.
 * Using HashTable, O(n) time, and O(n) space
 */
public class LC350IntersectionofTwoArrays2 {
    public int[] intersect(int[] nums1, int[] nums2) {
        ArrayList<Integer> tmp = new ArrayList<>();
        HashMap<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums1.length; i++) {
            if (map.containsKey(nums1[i])) {
                map.put(nums1[i], map.get(nums1[i] + 1));
            } else {
                map.put(nums1[i], 1);
            }
        }
        for (int j = 0; j < nums2.length; j++) {
            if (map.containsKey(nums2[j]) && map.get(nums2[j]) > 0) {
                tmp.add(nums2[j]);
            }
            map.put(nums2[j], map.get(nums2[j]) - 1);
        }
        int[] res = new int[tmp.size()];
        for (int k = 0; k < tmp.size(); k++) {
            res[k] = tmp.get(k);
        }
        return res;
    }
}
