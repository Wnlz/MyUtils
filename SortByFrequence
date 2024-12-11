// 1. 根据出现次数对字符串数组进行排序（降序，次数多的在前）
import java.util.Arrays;
import java.util.List;
import java.util.Map;
import java.util.function.Function;
import java.util.stream.Collectors;

public List<String> getFrequencyOfArray(String[] varNames) {
    // 获取所有 varName 的出现次数
    Map<String, Long> varNameCountMap = Arrays.stream(varNames)
            .filter(varName -> varName != null && !varName.isEmpty())
            .collect(Collectors.groupingBy(Function.identity(), Collectors.counting()));
    // 根据出现次数排序
    List<String> sortedArray = varNameCountMap.entrySet().stream()
            .sorted(Map.Entry.<String, Long>comparingByValue().reversed())
            .map(Map.Entry::getKey)
            .collect(Collectors.toList());
    return sortedArray;
}
