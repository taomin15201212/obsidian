创建

npx create-react-app my-app  

npm init react-app my-app

yarn create react-app my-app

  

启动

`npm start` or `yarn start`

  

【React】

插件 ：React router

import { Link } from 'react-router'

const { title } = this.props;

const {menuId,userName} = this.props.location.query; 取URL参数

周期函数：getInitialSate

【组件】

结构：

static get propTypes() {

    return {

      title: PropTypes.string

    };

  }

constructor(props) {

    super(props);

    this.state = {

    };

  }

<GaoNavInput/>



【React Native】

react-native init myapp

react-native run-android

启动Android Emulator

@ceho off

dir d:

call D:\Android\sdk\tools\emulator.exe -netdelay none -netspeed full -avd Nexus_5X_API_24

pause