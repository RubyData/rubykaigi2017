namespace :docker do
  desc 'Build docker image'
  task :build do
    sh 'docker', 'build', '-t',  'rubydata/rubykaigi2017', File.expand_path('..', __FILE__)
  end

  desc 'Pull docker image'
  task :pull do
    sh 'docker pull rubydata/rubykaigi2017'
  end

  desc 'Run docker container'
  task :run do
    sh 'docker', 'run', '-it', '--rm', '-p', '8888:8888', 'rubydata/rubykaigi2017'
  end

  namespace :run do
    desc 'Run docker container with attaching local volume'
    task :local do
      sh 'docker', 'run', '-it', '--rm', '-p', '8888:8888', '-v', "#{Dir.pwd}:/rubykaigi2017", 'rubydata/rubykaigi2017'
    end
  end
end
