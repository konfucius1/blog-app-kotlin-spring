# Key Takeaways

- Kotlin built-in null-safety prevent `NullPointerExceptions` at compile time
- Spring Framework provides null-safety for its API through tooling annotations, which can be used in conjunction with Kotlin's support for JSR 305 annotations to provide null-safety for the whole Spring Framework API
- jackson-module-kotlin</code> adds support for serialization/deserialization of Kotlin classes and data classes (single constructor classes can be used automatically, and those with secondary constructors or static factories are also supported)
- `@Bean` is used to indicate that a method produces a bean to be managed by the Spring container. When a class is annotated with
  ```
  @Configuration
  public class MyConfig {
      @Bean
      public MyBean myBean() {
          return new MyBean();
      }
  }
  ```
  `myBean()` returns an instance of `MyBean` &rarr; bean in Spring app. Once registered, the bean can be **injected** into other parts of the application, such as other beans or controllers, using `@Autowired`
