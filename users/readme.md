## GraphiQL queries

    {
      user(id:"40") {
        id,
        firstName,
        age
      }
    }

    // named query with fragment
    query findCompany {
      apple: company(id: "1") {
        ...companyDetails
        users {
          id
          firstName
          age
          company {
            name
          }
        }
      }
      google: company(id: "2") {
        ...companyDetails
        users {
          id
          firstName
          age
          company {
            name
          }
        }
      }
    }
    
    fragment companyDetails on Company {
      id
      name
      description
    }

## GraphiQL Mutations

    mutation {
      addUser(firstName: "Stephen", age: 26) {
        id
        firstName
        age
      }
    }
    
    mutation {
      deleteUser(id: "NwwSV6k") {
        id
      }
    }
    
    mutation {
      editUser(id: "40", age: 10) {
        id,
        firstName,
        age
      }
    }
