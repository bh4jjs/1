# vuep
前端vue+vuetify+axios，服务器golang

"dependencies": {
    "axios": "^0.19.2",
    "less": "^3.11.1",
    "style-loader": "^1.2.1",
    "vue": "^2.6.11",
    "vue-router": "^3.3.1",
    "vue-template-compiler": "^2.6.11",
    "vuetify": "^2.2.30",
    "vuetify-loader": "^1.4.4"
  },
  "devDependencies": {
    "@babel/core": "^7.10.1",
    "babel-loader": "^8.1.0",
    "babel-plugin-dynamic-import-webpack": "^1.1.0",
    "css-loader": "^3.5.3",
    "deepmerge": "^4.2.2",
    "fibers": "^5.0.0",
    "file-loader": "^6.0.0",
    "html-webpack-plugin": "^4.3.0",
    "material-design-icons-iconfont": "^5.0.1",
    "mini-css-extract-plugin": "^0.9.0",
    "optimize-css-assets-webpack-plugin": "^5.0.3",
    "sass": "^1.26.5",
    "sass-loader": "^8.0.2",
    "terser-webpack-plugin": "^3.0.2",
    "url-loader": "^4.1.0",
    "vue-loader": "^15.9.2",
    "vue-style-loader": "^4.1.2",
    "webpack": "^4.43.0",
    "webpack-cli": "^3.3.11",
    "webpack-dev-server": "^3.11.0"
  }
  
package main

import (
	...
)

func main() {
	log.SetFlags(log.Lshortfile | log.LstdFlags)

	environment()
	InitMasterDB()
	UpdateDB()
	
	c := cron.New()
	_, _ = c.AddFunc("1 0 * * *", Backup)
	c.Start()
  ...
}

