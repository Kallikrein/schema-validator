# schema-validator
validates a schema and outputs an error object


INTENT

```javascript
const schema = {
	email: {
		type: "email",
		required: true,
		errors: {
			type: "Please enter a valid email"
			required: "Please enter an email"
		}
	},
	password: {
		required: true,
		minLength: 8,
		errors: {
			required: "Please enter a password",
			minLength: "Your password should be at least 8 characters long"
		}
	}
};
validate = validator(schema);
```


```javascript
const JSONschema = {
	email: {
		type: "email",
		required: true,
	},
	password: {
		required: true,
		minLength: 8
	}
};
const errors = {
	email: {
		type: "Please enter a valid email",
		required: "Please enter an email"
	},
	password: {
		required: "Please enter a password",
		minLength: "Your password should be at least 8 characters long"
	}
};

validate = validator(JSONschema, errors);
```

```javascript
const reduxFormConfig = {
	form: "login-form",
	fields: [
		"email",
		"password"
	],
	validate
}
export default reduxForm(reduxFormConfig)(LoginContainer)
```
