# Jaxongirmirzo Rahimov

---

## Contact information:

- **Phone:** +99891-350-03-021
- **E-mail:** rjohongirmirzohon@gmail.com
- **Linkedin:** https://www.linkedin.com/in/johongir-rahimov-37584a1a5/
- **GitHub:** https://github.com/Johongirmirzo

---

## About Myself:

I'm a full-stack web developer who has been learning web development for 2 years. So far I've worked as the mentor and taught young aspiring developers web development technologies and helped them become developers. I'm very passionate about programming as it puts me in discomfort zone and challenges to push through which in the end helps me grow. Currently, I'm writing blogs on Dev.io to share my knowledge. My goals are building influencial applications that solve the real worl prolbems and make the world better place.

---

## Skills and Proficiency:

- HTML
- CSS (Framework Bootstrap, Preprocessor SCSS, BEM methodology).
- JavaScript (Fundamentals,Functional Programming, OOP, Asynchronous JavaScript, ES6+,DOM)
- TypeScript
- React
- Redux/Redux-Toolkit
- Node, Express
- Mongodb
- Git, GitHub

---

## Code examples

Theme Changer - Personal App

```JavaScript
import React, { useContext } from "react";
import { Button } from "@chakra-ui/react";
import { BsFillMoonFill, BsFillSunFill } from "react-icons/bs";
import { ThemeContext } from "../../context/ThemeContext";

const ThemeChanger = () => {
  const { toggleTheme, isLightMode } = useContext(ThemeContext);
  console.log(isLightMode);
  return (
    <Button
      bgColor="transparent"
      _hover="transparent"
      _active="transparent"
      onClick={toggleTheme}
    >
      {isLightMode ? (
        <BsFillSunFill style={{ fontSize: "25px" }} />
      ) : (
        <BsFillMoonFill style={{ fontSize: "20px" }} />
      )}
    </Button>
  );
};

export default ThemeChanger;
```

Register logic - Personal App

```JavaScript
    registerUser: async (req: Request, res: Response, next: NextFunction) => {
        try {
            const {username, email, password} = req.body;

            const user = await User.findOne({$and: [{username}, {email}]});
            if(user){
              return  res.send(["Username already exists", "Email already exists"])
            }
            const userDuplicate = await User.findOne({username});
            if(userDuplicate){
                return res.send(["Username already exists"])
            }
            const emailDuplicate = await User.findOne({email});
            if(emailDuplicate){
                return res.send(["Email already exists"])
            }

            const hashedPassword = await bcrypt.hash(password, 10);
            await User.create({
                username,
                email,
                password: hashedPassword
            })
            res.status(201).json({message: "User is successfully created"})
        }catch(err){
           return next(err)
        }
    },
```

---

## Coding Experience:

- [Kanban Server](https://github.com/Johongirmirzo/kanban-server)
- [Kanban UI](https://github.com/Johongirmirzo/kanban-ui)

- [Daily Sleep Tracker UI](https://github.com/Johongirmirzo/dst-ui)
- [Daily Sleep Tracker Server](https://github.com/Johongirmirzo/dst-server)

- [Markdown UI](https://github.com/Johongirmirzo/markdown-ui)

---

## Experience:

- **Full-Stack Developer Mentor at UITC Namangan**
  - Taught technologies of the web for beginners

---

## Education, Training:

- **FreeCodeCamp**
- **Odin Project**
- **Udemy**

---

## Languages:

- **Uzbek** - Native
- **Russian** - A2
- **English** - B2
- **Polish** - A2

---

## Hobbies:

- Reading, Calisthenics, Meditating, Philosophy

## Personal Qualities:

- Responsible, Punctual, Leadership, Time-Management, Good communication skills, Fast learning, Critical thinking, Multitasking.
