```
.
├── public/                          # 公共资源目录
│   ├── favicon.ico                  # 网站图标
│   └── logo.svg                     # 网站Logo
├── src/                             # 项目源代码目录
│   │── api                          # API请求封装函数
│   │   ├── home/                    # 首页业务接口目录
│   │   └── login/                   # 登录业务接口目录 
│   ├── assets/                      # 静态资源目录
│   │   ├── icons/                   # 图标资源目录
│   │   ├── images/                  # 图片资源目录
│   │   ├── js/                      # 脚本资源目录
│   │   └── styles/                  # 样式资源目录
│   ├── components/                  # 公共组件目录
│   ├── directives/                  # 公共指令目录
│   ├── layout/                      # 布局组件目录
│   ├── plugins/                     # plugins目录
│   ├── router/                      # 路由器目录
│   │   └── index.js                 # 路由器配置文件
│   ├── store/                       # 状态管理目录
│   │   ├── modules/                 # 模块化状态管理目录
│   │   ├── index.js                 # 状态管理配置文件
│   │   └── utils.js                 # 状态管理方法文件
│   ├── style/                       # 公共样式目录
│   │   ├── index.scss               # main样式文件
│   │   ├── reset.scss               # 重设样式文件
│   │   └── theme.scss               # 主题样式文件
│   ├── utils/                       # 工具函数目录
│   │   ├── request.js               # API请求封装函数
│   │   ├── auth.js                  # 鉴权相关函数
│   │   └── index.js                 # 辅助函数
│   ├── views/                       # 页面视图目录
│   │   ├── basic/                   # 基础模块相关视图目录
│   │   ├── home/                    # 首页相关页面目录
│   │   └── login/                   # 登录相关页面目录
│   ├── App.vue                      # 根组件
│   ├── main.js                      # 项目入口文件
│   ├── permission.js                # 路由拦截器权限控制逻辑文件
│   └── setting.js                   # 项目配置文件
├── .env                             # 环境配置文件
├── .editorconfig                    # 编辑器配置文件
├── .prettierrc                      # Prettier配置文件
├── commitlint.config.js             # CommitLint配置文件
├── jsconfig.js                      # JavaScript配置文件
├── .eslintrc.js                     # ESLint配置文件
├── Dockerfile                       # docker配置文件
├── vite.config.js                   # vite配置文件
├── index.html                       # 入口HTML文件
├── package.json                     # 项目依赖及配置文件
└── README.md                        # 项目说明文件
```
