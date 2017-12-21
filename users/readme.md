## GraphiQL queries

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
