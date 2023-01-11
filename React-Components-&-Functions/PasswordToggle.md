# 비밀번호 보이기 감추기

```js
import React, { useState } from "react";
import styled from "styled-components";

interface PropsType {
  type: string;
  placeholder: string;
  showButton: boolean;
  src: string;
  onchange: any;
}

const PWToggle = ({
  type,
  placeholder,
  showButton,
  src,
  onchange,
}: PropsType) => {
  const [passwordType, setPasswordType] = useState({
    type: "password",
    visible: false,
  });
  const handlePasswordType = () => {
    setPasswordType(() => {
      if (!passwordType.visible) {
        return { type: "text", visible: true };
      }
      return { type: "password", visible: false };
    });
  };
  return (
    <div className="pwtoggle">
      {type !== "password" ? (
        <input
          type={type}
          placeholder={placeholder}
          onChange={(e) => onchange(e.target.value)}
        ></input>
      ) : (
        <input
          type={passwordType.type}
          placeholder={placeholder}
          onChange={(e) => onchange(e.target.value)}
        />
      )}
      {showButton && (
        <button onClick={handlePasswordType}>
          <StImage src={src} toggle={passwordType.visible} />
        </button>
      )}
    </div>
  );
};

export default PWToggle;

const StImage = styled.div<{ src: string; toggle: boolean }>`
  width: 18px;
  height: 17px;
  background-image: url(${(props) => props.src});
  background-position: center;
  background-size: cover;
  opacity: ${(props) => (props.toggle ? "30%" : "")};
  cursor: pointer;
`;

```

# 사용
```js

const [pw, setPW] = useState("");

 <PWToggle
    type="password"
    placeholder="password"
    showButton={true}
    src={PWToggleImage}
    onchange={setPW}
  />
  
  ```
  
  # 이미지 예제 svg
 - PWToggleImage.svg
 ```js
 <svg width="19" height="19" viewBox="0 0 19 19" fill="none" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M18.4507 9.55675C17.752 8.39232 16.923 7.33079 15.9834 6.39758L7.1123 16.2309C7.89792 16.514 8.71825 16.661 9.54433 16.6667C14.8602 16.6667 18.3064 10.6976 18.4507 10.4434C18.6043 10.1724 18.6043 9.82778 18.4507 9.55675Z" fill="#B1C2D0"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M17.5931 1.07756C17.2997 0.752794 16.8244 0.752794 16.5309 1.07756L13.4801 4.45922C12.2703 3.73516 10.9194 3.34874 9.54455 3.33339C4.22868 3.33339 0.782507 9.30256 0.638164 9.55672C0.484544 9.82775 0.484544 10.1724 0.638164 10.4434C1.6226 12.0719 2.85932 13.4944 4.29108 14.6451L2.24698 16.9109C2.04691 17.1189 1.96489 17.4311 2.03297 17.7256C2.10106 18.0201 2.30844 18.2502 2.57409 18.3259C2.83974 18.4016 3.12149 18.3109 3.30925 18.0892L17.5931 2.25589C17.8866 1.93047 17.8866 1.40297 17.5931 1.07756ZM6.53741 10.0001C6.53741 8.15911 7.88375 6.66672 9.54455 6.66672C10.0787 6.66984 10.6019 6.83529 11.0571 7.14506L6.96894 11.6759C6.68993 11.1713 6.54071 10.5918 6.53741 10.0001Z" fill="#B1C2D0"/>
</svg>
```

  
