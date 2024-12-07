package com.klef.jfsd.exam;

import javax.persistence.*;

@Entity
@Table(name = "projects")
public class Project {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

  @Column(name = "project_name")
    private String projectName;

   private int duration; // in months
    private double budget; // in currency units

  @Column(name = "team_lead")
    private String teamLead;

  // Constructors, getters, and setters
    public Project() {}

  public Project(String projectName, int duration, double budget, String teamLead) {
        this.projectName = projectName;
        this.duration = duration;
        this.budget = budget;
        this.teamLead = teamLead;
    }

    / Getters and Setters
}
