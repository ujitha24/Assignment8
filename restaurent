import java.util.*;

public class restaurent {
    public static void main(String[] args) {
        List<Integer> ratings = Arrays.asList(4, 7, 8, 3, 6, 9, 5, 2, 10, 5);

        // Initialize maps to store counts and total ratings for each range
        Map<String, Integer> counts = new HashMap<>();
        Map<String, Integer> totalRatings = new HashMap<>();

        // Define rating ranges
        int[] ratingRanges = {1, 5, 6, 10};

        // Initialize counts and total ratings for each range
        for (int i = 0; i < ratingRanges.length; i += 2) {
            String range = ratingRanges[i] + "-" + ratingRanges[i + 1];
            counts.put(range, 0);
            totalRatings.put(range, 0);
        }

        // Calculate counts and total ratings for each range
        for (int rating : ratings) {
            for (int i = 0; i < ratingRanges.length; i += 2) {
                if (rating >= ratingRanges[i] && rating <= ratingRanges[i + 1]) {
                    String range = ratingRanges[i] + "-" + ratingRanges[i + 1];
                    counts.put(range, counts.get(range) + 1);
                    totalRatings.put(range, totalRatings.get(range) + rating);
                    break;
                }
            }
        }

        // Calculate average rating for each range and print results
        System.out.println("Restaurant Rating Analysis:");
        for (String range : counts.keySet()) {
            int numRestaurants = counts.get(range);
            int totalRating = totalRatings.get(range);
            double averageRating = (double) totalRating / numRestaurants;
            System.out.println("Range: " + range);
            System.out.println("Number of Restaurants: " + numRestaurants);
            System.out.println("Average Rating: " + averageRating);
            System.out.println();
        }
    }
}
