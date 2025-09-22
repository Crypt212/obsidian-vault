The core problem is that the way we structure data in object-oriented programming ([[OOP]]) is fundamentally different from how it's stored in most databases.

- **Objects** have inheritance, references to other objects, and complex hierarchies.
    
- **Relational Databases** have tables, rows, columns, and foreign keys. They are flat and relational.
    
- **Document Databases** have flexible, nested JSON-like structures. They are hierarchical but lack strict schemas and joins.
    

This fundamental difference is called the **Object-Relational Impedance Mismatch** (a term coined for relational DBs). The "impedance mismatch" for document databases is less severe because documents can more easily represent objects, but it still exists (e.g., handling data types, references, and schema validation).