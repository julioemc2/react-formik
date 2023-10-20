# React Formik

Este es un paquete de uso de React Formik

### Julio Galindo

## Ejemplo
```
import { useFormik } from "formik";
```

```
export const FormikBasicPage = () => {


    const { handleChange, values, handleSubmit } = useFormik({
        initialValues: {
            firstName: '',
            lastName: '',
            email: '',
        },
        onSubmit: values => {
            console.log(values);
        }
    });



  return (
    <div>
        <h1>Formik Basic Tutorial</h1>

        <form onSubmit={ handleSubmit } noValidate>
            <label htmlFor="firstName">First Name</label>
            <input 
                type="text"
                name="firstName"
                onChange={ handleChange }
                value={ values.firstName }
            />
            <span>First name is required</span>

            <label htmlFor="firstName">Last Name</label>
                <input 
                    type="text"
                    name="lastName"
                    onChange={ handleChange }
                    value={ values.lastName }
                />
                <span>Last name is required</span>

            <label htmlFor="firstName">Email Address</label>
                <input 
                    type="email"
                    name="email"
                    onChange={ handleChange }
                    value={ values.email }
                />
                <span>Email is required</span>
                <span>Check for a valid email format</span>

            <button type="submit">Submit</button>


        </form>
    </div>
  )
}
```