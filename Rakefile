def open_url(url)
  `open -a '/Applications/Google Chrome.app' #{url}`
end

def execute(cmd, args)
  cmd.gsub!('<project-name>', args[:project_name]) unless args[:project_name].nil?
  puts cmd
  IO.popen('pbcopy', 'w') { |f| f << cmd }
end

# Vue.js
desc 'Create the Vue.js app.'
task :vue, :project_name do |task, args|
  execute('vue create <project-name>', args)
end
task :vue_web do
  open_url('https://jp.vuejs.org/')
end

namespace :vue do
  desc 'Using the webpack template.'
  task :webpack, :project_name do |task, args|
    execute('vue create <project-name>', args)
  end

  desc 'Using the Electron template.'
  task :electron, :project_name do |task, args|
    execute('vue init simulatedgreg/electron-vue <project-name>', args)
  end
end

# Nuxt.js
desc 'Create the Nuxt.js app.'
task :nuxt, :project_name do |task, args|
  execute('yarn create nuxt-app <project-name>', args)
end
task :nuxt_web do
  open_url('https://ja.nuxtjs.org/')
end

# GAS
desc 'Create the Google Apps Script.'
task :gas, :project_name do |task, args|
  cmd  = 'mkdir <project-name> && '
  cmd += 'cd <project-name> && '
  cmd += 'clasp create --rootDir src --type webapp <project-name>'
  execute(cmd, args)
end

# React
desc 'Create the React app.'
task :react, :project_name do |task, args|
  execute('npx create-react-app <project-name>', args)
end
task :react_web do
  open_url('https://ja.reactjs.org/')
end

namespace :react do
  desc 'Using TypeScript.'
  task :ts, :project_name do |task, args|
    execute('npx create-react-app <project-name> --typescript', args)
  end
end

# ReactNative
desc 'Create the ReactNative app.'
task :reactnative, :project_name do |task, args|
  execute('npx react-native init <project-name>', args)
end
task :reactnative_web do
  open_url('https://facebook.github.io/react-native/')
end

namespace :reactnative do
  desc 'Using TypeScript.'
  task :ts, :project_name do |task, args|
    execute('npx react-native init <project-name> --template react-native-template-typescript', args)
  end
end

# ReactNative + Expo
desc 'Create the ReactNative + Expo app.'
task :expo, :project_name do |task, args|
  execute('expo init <project-name>', args)
end
task :expo_web do
  open_url('https://expo.io/')
end

# Electron
desc 'Create the Electron app.'
task :electron, :project_name do |task, args|
  execute('yarn create electron-app <project-name>', args)
end
task :electron_web do
  open_url('https://electronjs.org/')
end
