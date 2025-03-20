# Chapter 4: Data Transformation with dbt

## dbt Design Philosophy

- Code-centric apporach
    - dbt encourages users to define data transformation using code, promoting collaboration, version control and automation
- Modularity for reusability
    - dbt promotes modularity, allowing reusable code components, by models, macros and tests
- Transformations as SQL SELECT statements
    - This design choice simplifies development and ensures SQL best practices
- Declarative language
    - dbt uses a declarative language for defining data transformations
    - This abstraction reduces the complexity of writing complex SQL code and enhances readability
- Incremental builds
    - Allow updates only on the affected pieces
- Documentation as code
    - Descriptions, explanations, and metadata are stored alongside the project code, making it easier for team members to understand and collaborate effectively
- Data quality, testing and validation
    - Provides a testing framework that enables analysts to define data quality checks and validation rules
- Version control integration
    - Enables collaborative development, change tracking,
    and the ability to roll back changes
- Native integration with data platforms
    - Leverages the native capabilities of these plat‐
    forms for scalability and performance
- Open source and extensible
    - Users can extend its functionality by creating custom macros and packages. This extensibility allows organizations to tailor dbt to their specific data needs
- Separation of transformation and loading
    - dbt separates the transformation and loading steps in the data pipeline. Data is transformed within dbt and then loaded into the data platform