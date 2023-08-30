# How to use the useParams hook
#### As explained in the section above, you can declare a route with URL parameters so that React router dynamically captures the corresponding values in the URL when there is a match. It is useful when dynamically rendering the same component for multiple paths.
```jsx 
<Routes>
  <Route path="/blog/:id" element={<Blog />} /> 
</Routes>
```
#### Assuming you have the route above in your React router setup, you can retrieve the route parameters in the Blog component using the useParams hook. It returns an object. The object keys are the parameter names declared in the path string in the Route definition, and the values are the corresponding URL segment from the matching URL. You can use the useParams hook in the rendered component to retrieve the parameters like so:

```jsx 
import { useParams } from "react-router-dom";

const Blog = () => {
  const routeParams = useParams();
};
```
#### If the matching route is/blog/use-params for the example above, the useParams hook will return the object below. You can then use the returned object in the rendered Component the way you want.

```jsx
{
  id: "use-params"
}
```
# Conclusion
#### The useParams hook has been part of React router since version 5. It comes in handy if you want to retrieve route parameters from the functional component rendered by the matching route. The React Router useParams hook returns an object whose keys are the parameter names declared in the path string in the Route definition, and the values are the corresponding URL segment from the matching URL.