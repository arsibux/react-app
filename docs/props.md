# React Props
  Props stand for **"properties"**  immuteable or read only attributes of a components.
  It stores the values of attributes of a tag `<Components name="Ali"  age="25" hieght="5.8"/>`.

  ![component props](https://github.com/arsibux/react-app-overview/blob/main/docs/img/props.jpg "component props")

  ```
  function Student(props){
    return (
      <>
        <div className="student-profile-container">
          <div className="name">{prop.name}</div>
          <div className="name">{prop.age}</div>
          <div className="name">{prop.height}</div>
        </div>
      </>
    );
  }

  ```