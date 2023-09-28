# General study purpose
1. If we are preparing for exam following prompts can help preparing note
* Need answer according to marks

      {Type Question here}. I need an answer for this question for {marks} marks


* Need difference between in table

      {Type Question here}. Provide Difference between in table format


* For getting explaination on specific topic

      Explain me {topic} considering me as noob 

      Explain me {topic} considering me as new in this field 

      Explain me {topic} considering me as I am in grade one 

      Explain me {topic} with relatable example

# Designing product or Idea Clarification              
  
* Considering we are a designing a 3d printer that is controlled by web app

> In such situation we need to explain clearly what's we are trying to achieve and then what's our situation like what material do we have, which technology are we going to use and how it need to operate.
Although, It is going to be long prompt but output from this prompt is a lot better than just asking how can I design a system for operating the 3d printer from the web app.
Even if we do not get the expected answer we can analyze the output and refine the prompt accordingly which we will later in this page. So lets write the prompt for above prompt

        I am Designing a 3d printing system that can be controlled from the web app. Here what we are trying to achieve is we can just upload a 
        3d model and just on clicking the print button we should be able to print the model. we want 3d printer to be wireless we so I need you to provide following help
        1. what are necessary for designing such system
        2. what type of hardware and software and other third parties technologies do I need



> Here it provides Hardware and sofware requrements with some additional details. we can also go deep by asking about hardware components or any one we do not understand and also can refine previous prompt for better result
        


# For Programmer/Coder

1. Generative AI could be of very big help in debugging and just writing code faster
(incase of emergency we can do our 3X faster) 
* Prompt for Debugging proper
            ``` {Paste the code here, those code in which you suspect the error}
            Explain the what is this code suppose to do and what is current result of code 
            ```
 Example: 
        Consider the React Router Problem where we forget <Routes> tag
      ```
            import ReactDOM from "react-dom/client";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Layout from "./pages/Layout";
import Home from "./pages/Home";
import Blogs from "./pages/Blogs";
import Contact from "./pages/Contact";
import NoPage from "./pages/NoPage";

export default function App() {
  return (
    <BrowserRouter>
    
        <Route path="/" element={<Layout />}>
          <Route index element={<Home />} />
          <Route path="blogs" element={<Blogs />} />
          <Route path="contact" element={<Contact />} />
          <Route path="*" element={<NoPage />} />
        </Route>
    
    </BrowserRouter>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);

This is my code for the React Router but it is giving me error message{error message}
Provide me the code fixed also show me where I got wrong
        ```         
}

* if above condition is unable to solve the error properly then you can try following
            ```{paste the all code associate with the error. if code are in multiple file you can code according to the file}
            Now Here Explain the work flow in short and what error is occuring and what should be the output 

            ```
 Example:  
 if above process does not works then we can provide it with more information as error could also occur due to code in another file so this time we provide it code of other files related to routing too

      ```
      I was setting up react router and I got error. Following is the all code related to react router Provide me the mistake I have done with solution

      index.js
      import ReactDOM from "react-dom/client";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Layout from "./pages/Layout";
import Home from "./pages/Home";


export default function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Layout />}>
          <Route index element={<Home />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);

Layout.js
import { Outlet, Link } from "react-router-dom";

const Layout = () => {
  return (
    <>
      <nav>
        <ul>
          <li>
            <Link to="/">Home</Link>
          </li>
          <li>
            <Link to="/blogs">Blogs</Link>
          </li>
          <li>
            <Link to="/contact">Contact</Link>
          </li>
        </ul>
      </nav>

      <Outlet />
    </>
  )
};

export default Layout;

Home.js
const Home = () => {
  return <h1>Home</h1>;
};

export default Home;

      ```
This is the way how I deal with errors nowadays and It have made me really easy
to debug now Lets discuss about the how can we speed up writing our code.