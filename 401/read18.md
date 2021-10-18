# Web App Security

## [Hibernate Many to Many](https://www.baeldung.com/hibernate-many-to-many)
### Hibernate Many to Many Annotation Tutorial
In this quick tutorial, we'll have a quick look at how the `@ManyToMany` annotation can be used for specifying this type of relationships in Hibernate.

![IMG](https://www.baeldung.com/wp-content/uploads/2017/09/New.png)

>As in this example emplyee_project table has 2 foriegn keys that from other tables, because many emplyees can work in many projects.
Which means it happens when multiple records in a table are associated with multiple records in another table. 

- We have an employee table with employee_id as its primary key and a project table with project_id as its primary key. A join table employee_project is required here to connect both sides.
- We can specifying this type of relationships in Hibernate by @ManyToMany annotation .
- we will use example to Summarize the many to many relationship this example shows the many-to-many association between two entities employee and project.
- any given employee can be assigned to multiple projects and a project may have multiple employees working for it, leading to a many-to-many association between the two.
-  We need to create the employee and project tables along with the employee_project join table with employee_id and project_id as foreign keys.
- Then preparation of the Maven dependencies and Hibernate configuration.

**The Model Classes :** Employee and Project need to be created with JPA annotations
-  Both the Employee class and Project classes refer to one another, which means that the association between them is bidirectional.
- In order to map a many-to-many association, we use the @ManyToMany, @JoinTable and @JoinColumn annotations. 
- The @ManyToMany annotation is used in both classes to create the many-to-many relationship between the entities.
- This association has two sides i.e. the owning side and the inverse side. the owning side is Employee so the join table is specified on the owning side by using the @JoinTable annotation in Employee class. 
- The @JoinTable is used to define the join/link table. In this case, it is Employee_Project.
- The @JoinColumn annotation is used to specify the join/linking column with the main table. 
<hr>

## [Security: a humorous overview](https://scholar.harvard.edu/files/mickens/files/thisworldofours.pdf)

- ### Security researchers have a problem with public relations they tells people what to do and what not without explination.

- ### Threat models (threat/solution)-> `give every threat a solution`
