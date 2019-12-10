def open_url(url)
  `open -a '/Applications/Google Chrome.app' #{url}`
end

# Vue.js
desc 'Create the Vue.js app.'
task :vue, :project_name do
  project_name = args[:project_name] || '<project-name>'
  puts "vue create #{project_name}"
end
task :vue_web do
  open_url('https://jp.vuejs.org/')
end

namespace :vue do
  desc 'Using the webpack template.'
  task :webpack, :project_name do |task, args|
    project_name = args[:project_name] || '<project-name>'
    puts "vue init Webpack #{project_name}"
  end

  desc 'Using the Electron template.'
  task :electron, :project_name do |task, args|
    project_name = args[:project_name] || '<project-name>'
    puts "vue init simulatedgreg/electron-vue #{project_name}"
  end
end

# Nuxt.js
desc 'Create the Nuxt.js app.'
task :nuxt, :project_name do |task, args|
  project_name = args[:project_name] || '<project-name>'
  puts "yarn create nuxt-app #{project_name}"
end
task :nuxt_web do
  open_url('https://ja.nuxtjs.org/')
end

# GAS
desc 'Create the Google Apps Script.'
task :gas, :project_name do |task, args|
  project_name = args[:project_name] || '<project-name>'
  puts "mkdir #{project_name}"
  puts "cd #{project_name}"
  puts "clasp create --rootDir src --type webapp #{project_name}"
end

# React
desc 'Create the React app.'
task :react, :project_name do |task, args|
  project_name = args[:project_name] || '<project-name>'
  puts "npx create-react-app #{project_name}"
end
task :react_web do
  open_url('https://ja.reactjs.org/')
end

namespace :react do
  desc 'Using TypeScript.'
  task :ts, :project_name do |task, args|
    project_name = args[:project_name] || '<project-name>'
    puts "npx create-react-app #{project_name} --typescript"
  end
end

# ReactNative
desc 'Create the ReactNative app.'
task :reactnative, :project_name do |task, args|
  project_name = args[:project_name] || '<project-name>'
  puts "npx react-native init #{project_name}"
end
task :reactnative_web do
  open_url('https://facebook.github.io/react-native/')
end

namespace :reactnative do
  desc 'Using TypeScript.'
  task :ts, :project_name do |task, args|
    project_name = args[:project_name] || '<project-name>'
    puts "npx react-native init #{project_name} --template react-native-template-typescript"
  end
end

# ReactNative + Expo
desc 'Create the ReactNative + Expo app.'
task :expo, :project_name do |task, args|
  project_name = args[:project_name] || '<project-name>'
  puts "expo init #{project_name}"
end
task :expo_web do
  open_url('https://expo.io/')
end

# Electron
desc 'Create the Electron app.'
task :electron, :project_name do |task, args|
  project_name = args[:project_name] || '<project-name>'
  puts "yarn create electron-app #{project_name}"
end
task :electron_web do
  open_url('https://electronjs.org/')
end
