# lucky-wheel使用说明
1. 安装lucky-wheel包
`npm install -S lucky-wheel`
2. render组件
```js
import LuckyWheel from 'lucky-wheel';

constructor(props) {
  super(props);
  this.state = {
    position: 0,
    isComplete: false
  }
}
handleLoadData = () => {
  setTimeout(() => {
    this.setState({
      position: 2,
      isComplete: true
    })
  }, 1000);
}
handleComplete = () => {
  this.setState({isComplete: false})
}

render() {
  return (
    <LuckyWheel
       onLoadData={this.handleLoadData}
       position={this.state.position}
       areaNum={7}
       cycle={10}
       isComplete={this.state.isComplete}
       onComplete={this.handleComplete}
	     TURNTABLE_BG={TURNTABLE_BG} // new added
	     TURNTABLE={TURNTABLE}// new added
	     POINTER={POINTER}// new added
    />
  )
}

```

## 💖 Support my projects
If you get some profit from this or just want to encourage me to continue creating stuff, there are few ways you can do it:

<a href="https://www.buymeacoffee.com/callmejm" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 150px !important;" ></a>