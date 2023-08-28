# Senior .NET Engineer Take-Home Assignment

## Introduction

Thank you for your interest in joining our team as a Senior .NET Engineer. As part of our hiring process, we'd like to assess your technical skills, problem-solving abilities, and attention to detail through a take-home assignment. This exercise is designed to evaluate not just your coding skills but also your understanding of design principles. While we estimate that this task should take a few hours, feel free to invest additional time to add any extra features or polish that you think would make your solution stand out.

## Objective

Create an ASP.NET Core Web API implementing the CQRS pattern for a `Person` entity.

**Entity - Person:**

- `Id` (Guid)
- `GivenName` (String)
- `Surname` (String)
- `Gender` (Enum)
- `BirthDate` (Date)
- `BirthLocation` (String)
- `DeathDate` (Date)
- `DeathLocation` (String)

## Tasks

### Setup

- Create a new ASP.NET Core Web API project.
- Use any storage mechanism you prefer, including in memory

### Command Model (Write Side)

- Implement a command to `AddPerson`.
- Implement a command to `RecordBirth`.
- Each command should have its handler.

### Query Model (Read Side)

- Implement a query to `GetPersonId`.
- Implement a query to `GetAllPeople`.
- Each query should have its handler.

### Validation

- Implement validation for the `AddPerson` command to ensure that at least one name and a gender are provided.
- Implement validation for the `RecordBirth` command to ensure that either `BirthDate` or `BirthLocation` is provided.

### Logging

- Introduce basic logging (using, for example, Serilog) to log when a command or query is handled.

### Bonus (if time allows)

- Implement a basic versioning system for the `Person` entity. Whenever a person is updated, store its previous version. Provide a query to retrieve the version history of a person.

### Expectations

1. **Architecture**: Clear separation between command and query responsibilities.
2. **Code Quality**: Clean, readable, and maintainable code.
3. **Validation**: Proper input validation for commands.
4. **Error Handling**: Handle possible errors gracefully. Return meaningful error messages and appropriate HTTP status codes.
5. **Logging**: Basic logging to trace the flow of commands and queries.
6. **Testing**: Include unit tests for command/query handlers and (Bonus) integration tests for API endpoints.
7. **Domain concepts (Bonus)**: If possible, implement domain entities for names, dates, gender, or locations that will be more robust than just using strings or DateTime types

### Deliverables

- A working ASP.NET Core Web API project implementing the above requirements.
- A public GitHub repository containing the code
- Documentation (can be a README file) explaining:
  - How to run the project.
  - Any assumptions made.
  - Any challenges faced and how they were addressed.
  - Future improvements if given more time.