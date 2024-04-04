import java.util.*;

class BookReview {
    private String title;
    private int rating;
    private String sentiment;

    public BookReview(String title, int rating) {
        this.title = title;
        this.rating = rating;
        this.sentiment = analyzeSentiment(rating);
    }

    private String analyzeSentiment(int rating) {
        if (rating >= 8) {
            return "Positive";
        } else if (rating >= 6) {
            return "Neutral";
        } else {
            return "Negative";
        }
    }

    public int getRating() {
        return rating;
    }

    public String getSentiment() {
        return sentiment;
    }
}

public class review {
    public static void main(String[] args) {
        List<BookReview> reviews = new ArrayList<>();
        reviews.add(new BookReview("Book1", 9));
        reviews.add(new BookReview("Book2", 3));
        reviews.add(new BookReview("Book3", 7));
        reviews.add(new BookReview("Book4", 5));
        reviews.add(new BookReview("Book5", 8));
        reviews.add(new BookReview("Book6", 4));

        // Initialize maps to store counts for rating ranges and sentiments
        Map<String, Integer> ratingRangeCounts = new HashMap<>();
        Map<String, Integer> sentimentCounts = new HashMap<>();
        sentimentCounts.put("Positive", 0);
        sentimentCounts.put("Neutral", 0);
        sentimentCounts.put("Negative", 0);

        // Define rating ranges
        int[] ratingRanges = {1, 5, 6, 10};

        // Calculate counts for rating ranges and sentiments
        for (BookReview review : reviews) {
            int rating = review.getRating();
            String sentiment = review.getSentiment();

            // Increment rating range counts
            for (int i = 0; i < ratingRanges.length; i += 2) {
                if (rating >= ratingRanges[i] && rating <= ratingRanges[i + 1]) {
                    String range = ratingRanges[i] + "-" + ratingRanges[i + 1] + " stars";
                    ratingRangeCounts.put(range, ratingRangeCounts.getOrDefault(range, 0) + 1);
                    break;
                }
            }

            // Increment sentiment counts
            sentimentCounts.put(sentiment, sentimentCounts.get(sentiment) + 1);
        }

        // Print results
        System.out.println("Book Review Analysis:");
        System.out.println("Rating Ranges:");
        for (String range : ratingRangeCounts.keySet()) {
            System.out.println(range + ": " + ratingRangeCounts.get(range) + " books");
        }
        System.out.println("\nSentiment Analysis:");
        for (String sentiment : sentimentCounts.keySet()) {
            System.out.println(sentiment + ": " + sentimentCounts.get(sentiment) + " books");
        }
    }
}
