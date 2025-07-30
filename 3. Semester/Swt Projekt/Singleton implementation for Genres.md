```java
import java.util.ArrayList;
import java.util.List;

public class Genre {
    private static final List<Genre> genres = new ArrayList<>();
    private final String name;

    private Genre(String name) {
        this.name = name;
    }

    public static Genre getGenre(String name) {
        String normalizedName = name.trim().toLowerCase();

        // Search in the list for an existing genre
        for (Genre genre : genres) {
            if (genre.name.equalsIgnoreCase(normalizedName)) {
                return genre;
            }
        }

        // If not found, create a new genre and add it to the list
        Genre newGenre = new Genre(name);
        genres.add(newGenre);
        return newGenre;
    }

    public static List<Genre> getAllGenres() {
        return genres;
    }

    @Override
    public String toString() {
        return "Genre{name='" + name + "'}";
    }
}

```