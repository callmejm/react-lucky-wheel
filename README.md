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

<style>.bmc-button img{width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#000000 !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/callmejm"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Treat me caffine"><span style="margin-left:15px;font-size:28px !important;">Treat me caffine</span></a>