### 子组件 父组件验证

父组件
```
组件引用
  <common-add :index="index" ref='child' v-model="dat.blockList[index]" @getChildComp="getChildComp"></common-add>

onSubmit () {
  Promise.all([this.checkValidate(), this.checkChildValidate()]).then(() => {
    if (this.id) {
      this.validatorSubmit('dat', 'post', this.updateapi, this.dat)
    } else {
      this.validatorSubmit('dat', 'post', this.addapi, this.dat)
    }
  }).catch(() => {
    console.warn('验证未通过')
  })
},
checkValidate () {
  return new Promise((resolve, reject) => {
    this.$refs['dat'].validate((valid) => {
      if (valid) {
        resolve()
      } else {
        reject()
        return false
      }
    })
  })
},
checkChildValidate () {
  return new Promise((resolve, reject) => {
    let arr = []
    this.$refs['child'].find((item, index) => {
      this.dat.blockList[index] = this.$refs['child'][index].dat
      arr.push(item.validateForm())
    })
    let flag = arr.find(item => item === true)
    if (!flag && flag !== undefined) {
      reject()
    } else {
      resolve()
    }
  })
},
```

**子组件**

```
validateForm () {
  let flag = false
  this.$refs['dat'].validate((valid) => {
    flag = valid
  })
  return flag
},
```
