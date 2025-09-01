## 开发

```bash
# 安装依赖
npm install

# 推荐使用yarn或者pnpm下载依赖
npm install yarn -g
yarn

npm install pnpm -g
pnpm i

# 启动服务
npm run dev
```

## 发布

```bash
# 构建测试环境
npm run build:stage

# 构建生产环境
npm run build:prod
```

## 目录划分

- 各模块业务相关页面在views下创建目录存放，api目录与views目录相对应。例如登录的vue文件放在`src/views/login`，对应的api存放在`src/api/login`
- 缓存在store下创建目录存放，例如登录相关的缓存存放在`src/store/modules/login`
- 如有图片新增在`src/assets/images`下创建目录存放，例如登录相关图片存放在 `src/assets/images/login`
- 如有图标新增在`src/assets/icons`下创建目录存放，例如登录相关图标存放在 `src/assets/icons/login`
- 如有模块样式新增在`src/assets/styles`下创建目录存放，例如登录相关样式存放在 `src/assets/styles/login`

```
.
├── docker/                          # docker配置目录
│   └── Dockerfile                   # docker配置文件
├── public/                          # 公共资源目录
│   ├── nginx.conf                   # nginx代理配置文件
│   └── favicon.ico                  # 网站图标
├── src/                             # 项目源代码目录
│   │── api                          # API请求封装函数
│   │   ├── home/                    # 首页业务接口目录
│   │   └── login/                   # 登录业务接口目录 
│   ├── assets/                      # 静态资源目录
│   │   ├── icons/                   # 图标资源目录
│   │   ├── images/                  # 图片资源目录
│   │   └── styles/                  # 样式资源目录
│   ├── components/                  # 公共组件目录
│   │   ├── ComponentA/              # 公共组件A目录
│   │   │   └── index.vue            # 公共组件A
│   │   └── ComponentB/              # 公共组件B目录
│   ├── hooks/                       # 公共封装hooks目录
│   ├── layout/                      # 布局组件目录
│   ├── router/                      # 路由器目录
│   │   └── index.ts                 # 路由器配置文件
│   ├── store/                       # 状态管理目录
│   │   ├── modules/                 # 模块化状态管理目录
│   │   └── index.ts                 # 状态管理配置文件
│   ├── utils/                       # 工具函数目录
│   │   ├── request.js               # API请求封装函数
│   │   ├── auth.js                  # 鉴权相关函数
│   │   └── index.ts                 # 辅助函数
│   ├── views/                       # 页面视图目录
│   │   ├── home/                    # 首页相关页面目录
│   │   └── login/                   # 登录相关页面目录
│   ├── App.vue                      # 根组件
│   └── main.js                      # 项目入口文件
├── tests/                           # 测试目录
│   ├── e2e/                         # 端到端测试目录
│   │   ├── specs/                   # 测试规范目录
│   │   └── Nightwatch.conf.js       # Nightwatch配置文件
│   └── unit/                        # 单元测试目录
│       ├── specs/                   # 测试规范目录
│       └── jest.config.js           # Jest测试配置文件
├── index.html                       # 入口HTML文件
├── .editorconfig                    # 编辑器配置文件
├── .eslintrc.cjs                    # ESLint配置文件
├── .prettierrc.js                   # Prettier配置文件
├── vite.config.js                   # vite配置文件
├── package.json                     # 项目依赖及配置文件
└── README.md                        # 项目说明文件
```

## 注意事项

- 基础表格页面布局参考：[比翼设计交互规范-表格](https://help.ctbiyi.com/biyi-design/ui-design/table.html)
   - 搜索区最多一行，超出一行收起隐藏，出现"展开"文字按钮；
   - 每行4个输入框或下拉框，不满4个时，按钮居右展示，正好满一行时，按钮另起一行；
   - 按钮样式参考：[比翼设计交互规范-按钮](https://help.ctbiyi.com/biyi-design/ui-design/button.html)
   - 输入框或下拉框高度设为32px，表格页面label在左侧居右，配置表单弹窗中label顶部居左，按钮高度一致也为32px；
   - 配置弹窗宽度：800px，高度小于800px，如超出滚动显示；提示类弹窗宽度400px，高度小于400px；特殊弹窗可自行定义宽高；
   - 表格操作按钮在表格上方一行，居右显示，按钮间距为10px；

## 开发样例
1. 文件命名规范：文件名应该清晰明了，有意义，使用小驼峰命名法。例如，`userProfile.vue`。

2. 代码格式规范：代码应该格式化好，易于阅读。开发时严格使用ESLint、Prettier等工具来保持代码格式的一致性和准确性。代码缩进应使用两个空格进行缩进，而不是制表符。

3. 变量命名规范：变量名应该清晰明了，有意义，使用小驼峰命名法。例如，`userProfile`。

4. 组件命名规范：组件名应该清晰明了，有意义，使用大驼峰命名法。例如，`UserProfile`。公共组件存入src/components目录，业务组件存入./components目录。

5. 注释规范：代码中应该有适当的注释，以便其他人能够理解您的代码。注释应该清晰明了，有意义。
- 业务注释模板
```
/**
* ${description}
* @author ${user}
* @date ${date} ${time}
*/
```
- 方法注释模板
```
**
 * ${description}
 * ${param}
 * @return ${return}
 * @author ${user}
 * @date ${date} ${time}
 */
```
6.

7. 单文件组件规范：在编写单文件组件时，应该将模板代码、脚本代码和样式代码分开，并按照一定的顺序排列。例如：

```
<template>
  <div>
    <!-- 模板代码 -->
  </div>
</template>

<script>
export default {
  name: 'UserProfile',
  // 脚本代码
}
</script>

<style scoped>
/* 样式代码 */
</style>
```
8. 其他规范：还有一些其他的规范，如避免使用全局变量、避免在模板中使用复杂的表达式、使用常量代替魔法数字等等。

## 分支情况

目前我们前端的代码分支情况如下：

- main分支   （Feature  branches）：每个sprint结束之后会将master分支合到该分支用于打tag包
- master分支 （Feature  branches）：产环境代码，测试通过之后会将test分支合并到该分支
- test分支   （Feature  branches）：测试环境代码，本地自测或则是开发环境自测完之后将自己创建的xxxx分支合并到该分支
- develop分支（Feature  branches）：开发环境的代码，本地自测完发布到开发环境的需要合并到该分支
- 功能分支    （Feature  branches）：当您开始开发一个新功能时，从develop分支创建一个新的功能分支。这个分支的名称应该描述您正在开发的功能。例如，如果您正在开发一个用户注册功能，那么您可以从develop分支创建一个名为feature/taskCodeOrExplain的功能分支。
- 修复分支    （Hotfix   branches）：如果您需要紧急修复一个已经发布的版本中的错误或缺陷，那么可以从master分支创建一个新的修复分支。这个分支的名称应该描述您正在修复的问题。例如，如果您需要修复一个密码重置链接错误，那么您可以从master分支创建一个名为hotfix/bugCodeOrExplain的修复分支
- 个人分支    （Personal branches）：如果您需要在开发过程中保存一些临时性的工作，可以从develop分支创建一个新的个人分支。这个分支的名称应该包含您的用户名或其他可以识别您的信息。例如，如果您的用户名是john，那么您可以从develop分支创建一个名为john/feature/work-in-progress的个人分支。
## 代码提交规范
目前我们前端的代码提交规范如下：
1. 提交类型（Type）：每个提交应该以一个描述性的提交类型开头，例如“feat”、“fix”、“docs”、“style”、“refactor”、“test”、“chore”等。下面是一些可能有用的类型及其含义：

- feat：添加新功能或功能性改进。
- fix：修复错误或缺陷。
- docs：修改文档或注释。
- style：修改代码格式或样式。
- refactor：重构代码，但不添加新功能或修复错误。
- test：添加或修改测试代码。
- chore：修改构建过程或辅助工具。

2. 范围（Scope）：如果您的提交涉及到特定部分的代码库，可以添加一个范围以更好地描述您的更改。例如，如果您在修改网站的登录页面，那么您可以在您的提交信息中指定“login”范围。

3. 提交信息（Subject）：在提交类型和范围之后，您应该提供一句简短的描述您的更改，这句话应该简明扼要，但又能够清楚地表达您的更改的目的。例如，“feat: 添加用户注册功能”或“fix(login): 修复密码重置链接错误”。

4. 提交详情（Body）：在提交信息之后，您可以添加更详细的说明，包括为什么要进行更改，以及更改的具体内容。这个部分可以帮助其他开发人员更好地理解您的更改，也可以作为以后查看历史记录时的参考。

5. 关联问题（Issue）：如果您的提交涉及到已知的问题或缺陷，您可以在提交信息中引用相关的问题编号。例如，“fix(login): 修复密码重置链接错误，解决问题#123”。

最后，一个示例提交信息可以是这样的：

```
feat(login): 添加用户注册功能

在登录页面添加了新的注册表单，以便用户可以创建新账户。

关联问题：#123
```




