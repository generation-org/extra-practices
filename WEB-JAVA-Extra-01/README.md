<img align="right" width="150" height="150" src="https://media-exp1.licdn.com/dms/image/C4E0BAQF7BYCCZt5epw/company-logo_200_200/0?e=2159024400&v=beta&t=qUAFP9bUgBEEXGVQYpUXW1J_OiP8e0r4rFBpqp8OrxA">

# WEB-JAVA-Extra-01 - Inventory Management System

 <br/>

## Exercise

In this exercise, you're going to create an inventory management system for a store. The system manages the items contained in a shop's inventory. You'll store items objects in a database and access them. Then wrap it with a controller.

### Tips

1. Go to <https://start.spring.io/> and add the following dependencies to a project:
    * Web
    * JPA
    * H2 (that's for the database)
2. Choose the name of your project and generate it
3. Define an generic "Item" class. Feel free to use the following piece of code as starting point:

```java
package inventory;

import java.util.Objects;

import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.Id;

@Entity
class Item {

  private @Id @GeneratedValue Long id;
  private String name;
  private String category;

  Item() {}

  Item(String name, String category) {

    // define the constructor
  }

  public Long getId() {
    // TODO
  }

  public String getName() {
    // TODO
  }

  public String getCategory() {
    // TODO
  }

  public void setId(Long id) {
    // TODO
  }

  public void setName(String name) {
    // TODO
  }

  public void setCategory(String category) {
    // TODO
  }

  @Override
  public boolean equals(Object o) {
    // TODO
  }

  @Override
  public int hashCode() {
    return Objects.hash(this.id, this.name, this.category);
  }

  @Override
  public String toString() {
    // TODO
  }
}
```

4. Create a JPA repository - simply an interface which extends Spring Data JPA’s JpaRepository, specifying the domain type as Item and the id type as Long. This allows you to create, update, delete and find items in your inventory.
5. Create your main class, to initialize the inventory application. Use the SpringBootApplication annotation in your main class.
6. Add a load database class, to load some items into your inventory database. This code should look like this:

```java
package inventory;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.boot.CommandLineRunner;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
class LoadDatabase {

  private static final Logger log = LoggerFactory.getLogger(LoadDatabase.class);

  @Bean
  CommandLineRunner initDatabase(ItemRepository repository) {

    return args -> {
    // What would you like your shop to sell? Create your inventory!
      log.info("Preloading " + repository.save(new Item("Item name", "item category"))); 
      
    };
  }
}
```

7. Finally, to wrap your repository with a web layer, you must add a Spring Controller. Use mappings to add routes that will:
    * Get all items in the inventory
    * Get a specific item, by id
    * Add a new item
    * Edit an existing item
    * Delete an item

