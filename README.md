# Cucumber Ruby skeleton
  Functional tests on any platform webapp. The tests are developed with Cucumber framework, Capybara for step definitions and Rspec for expect results. The project is structured with page objects concept (site_prism) and language Ruby. A report is created at the end of the run in HTML. Case upload the project at Github you can use Circle Ci for continous integration.

# The project is structured this way:

- project_name
    * cucumber
      + features
        * attach (path for attached files needed in the tests)
        * hooks
        * page_objects (works with site_prism gem for page objects pattern)
        * specifications (Cucumber BDD)
        * step_definitions (develop in Capybara, Ruby and Rspec)
        - support
          * config
          * knowledgebase
      + screenshots
        - test_passed
          * run_date
        - test_failed
          * run_date
      * cucumber.yml (for Circle ci)
      + features_report.json (works by generating html report utilizing the json file with Jenkins)
      + features_report.html (simple report in html with screenshot of expect results)
      
# Driver needed:
- For default, on my tests are executed on Chrome.
- Install Nodejs (Next, Next e Finish) https://nodejs.org/en/ and after the command below on terminal:

```ruby
npm install -g chromedriver
```

# Configuring the enviroment:
- Needed instalation ruby 2.3.3 and Devkit 64 bits.
- Install the bundler. Navigate on path \project_name and execute the follow command:

```ruby
gem install bundler
```

# Installing the gems:
- Execute this command below on root of project, path of project:

```ruby
bundle install
```

# Executing the tests:
- On path \project_name\cucumber, execute the command below for execution the all tests:

```ruby
cucumber
```

# Test Report in HTML:
After the tests are run a report will be available in the path \project_name\cucumber\features_report.html
Note: The screenshots will be available at the bottom of each report feature.
