import java.util.*;

public class TestScoreAnalyzer {
    public static void main(String[] args) {
        List<Integer> testScores = Arrays.asList(80, 75, 90, 85, 70, 95, 60, 65, 100, 55);

        // Calculate average score
        double averageScore = calculateAverage(testScores);

        // Calculate median score
        int medianScore = calculateMedian(testScores);

        // Count number of students above, at, and below average
        int aboveAverageCount = 0;
        int atAverageCount = 0;
        int belowAverageCount = 0;

        for (int score : testScores) {
            if (score > averageScore) {
                aboveAverageCount++;
            } else if (score == averageScore) {
                atAverageCount++;
            } else {
                belowAverageCount++;
            }
        }

        // Print results
        System.out.println("Test Score Analysis:");
        System.out.println("Average Score: " + averageScore);
        System.out.println("Median Score: " + medianScore);
        System.out.println("Number of students above average: " + aboveAverageCount + ", Median score: " + medianScore);
        System.out.println("Number of students at average: " + atAverageCount + ", Median score: " + medianScore);
        System.out.println("Number of students below average: " + belowAverageCount + ", Median score: " + medianScore);
    }

    // Method to calculate the average score
    private static double calculateAverage(List<Integer> scores) {
        int total = 0;
        for (int score : scores) {
            total += score;
        }
        return (double) total / scores.size();
    }

    // Method to calculate the median score
    private static int calculateMedian(List<Integer> scores) {
        Collections.sort(scores);
        int size = scores.size();
        if (size % 2 == 0) {
            return (scores.get(size / 2) + scores.get(size / 2 - 1)) / 2;
        } else {
            return scores.get(size / 2);
        }
    }
}
