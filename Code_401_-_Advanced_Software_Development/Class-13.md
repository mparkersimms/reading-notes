# Class 13 

## Spring data rest relationships

### One-to-One Relationship

The Data Model

```
@Entity
public class Library {

    @Id
    @GeneratedValue
    private long id;

    @Column
    private String name;

    @OneToOne
    @JoinColumn(name = "address_id")
    @RestResource(path = "libraryAddress", rel="address")
    private Address address;
    
    // standard constructor, getters, setters
}
```
```
@Entity
public class Address {

    @Id
    @GeneratedValue
    private long id;

    @Column(nullable = false)
    private String location;

    @OneToOne(mappedBy = "address")
    private Library library;

    // standard constructor, getters, setters
}

```

The Repositories

```
public interface LibraryRepository extends CrudRepository<Library, Long> {}
```
```
public interface AddressRepository extends CrudRepository<Address, Long> {}
```

### One-to-many relationship

The Data Model

```
@Entity
public class Book {

    @Id
    @GeneratedValue
    private long id;
    
    @Column(nullable=false)
    private String title;
    
    @ManyToOne
    @JoinColumn(name="library_id")
    private Library library;
    
    // standard constructor, getter, setter
}
```

```
public class Library {
 
    //...
 
    @OneToMany(mappedBy = "library")
    private List<Book> books;
 
    //...
 
}
```
### Many-to-Many Relationship

The Data Model

```
@Entity
public class Author {

    @Id
    @GeneratedValue
    private long id;

    @Column(nullable = false)
    private String name;

    @ManyToMany(cascade = CascadeType.ALL)
    @JoinTable(name = "book_author", 
      joinColumns = @JoinColumn(name = "book_id", referencedColumnName = "id"), 
      inverseJoinColumns = @JoinColumn(name = "author_id", 
      referencedColumnName = "id"))
    private List<Book> books;

    //standard constructors, getters, setters
}
```
```
public class Book {
 
    //...
 
    @ManyToMany(mappedBy = "books")
    private List<Author> authors;
 
    //...
}
```

