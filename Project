import java.util.*;

class Project {
    private String name;
    private int completionTime;

    public Project(String name, int completionTime) {
        this.name = name;
        this.completionTime = completionTime;
    }

    public int getCompletionTime() {
        return completionTime;
    }
}

class Student {
    private String name;
    private List<Project> projects;

    public Student(String name) {
        this.name = name;
        projects = new ArrayList<>();
    }

    public void addProject(Project project) {
        projects.add(project);
    }

    public List<Project> getProjects() {
        return projects;
    }

    public String getName() {
        return name;
    }
}

public class ProjectTracker {
    public static void main(String[] args) {
        List<Student> students = new ArrayList<>();
        students.add(new Student("Alice"));
        students.add(new Student("Bob"));

        // Adding projects for demonstration
        students.get(0).addProject(new Project("Project 1", 10));
        students.get(0).addProject(new Project("Project 2", 12));
        students.get(1).addProject(new Project("Project 1", 8));
        students.get(1).addProject(new Project("Project 2", 15));

        // Track completion status and average completion time for each student
        for (Student student : students) {
            int onTime = 0;
            int late = 0;
            int early = 0;
            int totalCompletionTime = 0;
            List<Project> projects = student.getProjects();

            for (Project project : projects) {
                int completionTime = project.getCompletionTime();
                totalCompletionTime += completionTime;

                if (completionTime == 10) { // Assuming 10 is the on-time completion time
                    onTime++;
                } else if (completionTime < 10) {
                    early++;
                } else {
                    late++;
                }
            }

            int numProjects = projects.size();
            double averageCompletionTime = (double) totalCompletionTime / numProjects;

            System.out.println("Student: " + student.getName());
            System.out.println("Projects Completed On Time: " + onTime);
            System.out.println("Projects Completed Early: " + early);
            System.out.println("Projects Completed Late: " + late);
            System.out.println("Average Completion Time: " + averageCompletionTime + " days");
            System.out.println();
        }
    }
}
