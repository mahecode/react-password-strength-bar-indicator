# react-password-strength-bar-indicator
# Overview

A simple npm package to implement password input with strength bar indicator to know the password strength.


# Installation
  Npm users
   
    $ npm install --save react-password-strength-bar-indicator



   
   Yarn users
   
    $ yarn add react-password-strength-bar-indicator



## Usage

 For Stateful components.

    import  PasswordInput  from  'react-password-strength-bar-indicator';
    import  "react-password-strength-bar-indicator/lib/main.css"
    
    class App extends React.Component {
    ...
	    this.state = {
		    password: '',
		    passwordStrength: '', // To get the values of strenght
		}
		render(){
			return(
				<PasswordInput
					value={this.state.password}
					onChange={e => this.setState({password: e.target.value})
					passwordStrength={value => this.setState({passwordStrength: value})
					placeholder="Password"
					type="password"
				/>
			)
		}
	}
For Stateless component.

    import  PasswordInput  from  'react-password-strength-bar-indicator';
    import  "react-password-strength-bar-indicator/lib/main.css"
    
    const App = () => {
	    const [password, setPassword] = useState("");
	    const [passwordStrength, setPasswordStrength] = useState("");
		
		return(
			<PasswordInput
				value={password}
				onChange={e => setPassword(e.target.value)
				passwordStrength={value => setPasswordStrength(value)
				placeholder="Password"
				type="password"
			/>
		)
	}

## Props


|           Props     |Value                          |Description                         |
|----------------|-------------------------------|-----------------------------|
|value|`input value`            |Input value            |
|onChange          |`onChange={e => func(e)}`            |to handle onchange password input |
|inputClassName          |`inputClasName`| To change the style for password input which takes className as a value|
|placeholder | `placeholder` | For password input placeholder
|disabled | `disabled={false}` | To disable the password input either true or false
|statusClassName | `statusClassName` | To change the style for status which is weak , fair and strong which takes className as a value
|passwordStrength | `passwordStrength={value => func(value)}` | PasswordStrength function which will return the current strength of password
|strengthStyle | `strengthStyle={{style}}` | StrengthStyle takes React style object to style the bar indicator.
|type | `type` | Type which can be either password or text field.



## License

MIT
