
* Comma Operator ( , ): The Comma operator evaluates each operand from left to right and returns the value of right most operand.
```
var a = 4;
a = (a++, a);
console.log("The value for expression with comma operator is: " + a)
```

* Condtional Operator
```
var num_of_months = 13
var ans = (num_of_months > 12) ? "Invalid" : "Valid"
```

* expression
```
this: points to the current object
super: calls methods on an object’s parent, for example, call parent’s constructor
function: used to define a function
function*: used to define a generator function
async function: used to define an async function
```

* react if else
```
export default class App extends React.Component {
  render() {
    const users = [
      { name: 'Robin' },
      { name: 'Markus' },
    ];

    const showUsers = true;
    if (!showUsers) {
      return null;
    }

    return (
      <ul>
        {users.map(user => <li>{user.name}</li>)}
      </ul>
    );
  }
}

```

* react ternary
```
export default class App extends React.Component {
  render() {
       const users = [
      { name: 'Robin' },
      { name: 'Markus' },
    ];
    const showUsers = true;
    return (
      <div>
        {
          showUsers ? (
            <ul>
              {users.map(user => <li>{user.name}</li>)}
            </ul>
          ) : (
            null
          )
        }
      </div>
    );
  }
}
```

* destructing

```
const student = {
  ID: '21',
  name: 'Jhon',
  GPA: '3.0',
};

const {ID, name, GPA} = student;
```

* destructuring alias
```
const student = {
  ID: '21',
  name: 'Jhon',
  GPA: '3.0',
};

const {name:n} = student;
console.log(n);
```

```
// no destructuring
const users = this.state.users;
const counter = this.state.counter;

// destructuring
const { users, counter } = this.state;
```

functional stateless components because they always receive the props object in their function signature.

```
// no destructuring
function Greeting(props) {
  return <h1>{props.greeting}</h1>;
}

// destructuring
function Greeting({ greeting }) {
  return <h1>{greeting}</h1>;
}
```

* array destruc
// rest destructuring
const { users, ...rest } = this.state;

* spread operator
```
a = [1,2,3];
b = [4,5,6];
c = a.concat(b);
console.log("c: " + c);
```

```
a = [1,2,3];
b = [4,5,6];
c = [...a, ...b]; //spread operator
console.log("c: " + c);
```

Spread Operator so handy in React
```
You can easily add some elements in the middle of the two arrays: [...a, 'something', ...b];
It’s simpler to use and also gives you a visual idea of what your array looks like.
You can clone arrays using this operator: clone = [...a];

const person = { name: "Jhon"};
const student = { ID: "21", GPA: "3.0"};

const new_object = { ...person, ...student, semester: '3'};
console.log(new_object);
```