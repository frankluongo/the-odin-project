# Your First Rails Application

[Your First Rails Application](https://www.theodinproject.com/courses/web-development-101/lessons/your-first-rails-application?ref=lnav)

## Introduction

The following command will print your username

```bash
whoami
```

## Your First Rails App

### Step 1: Create Your First Ruby on Rails Web Application

#### Step 1.1: Install Rails and Bundler

```bash
gem install rails -v 5.2.3
```

### Step 1.2: Lay the Groundwork

Create your directory

### Step 1.3: Create the Application

```bash
rails new rails_app_name
```

Scaffold out some data

```bash
rails generate scaffold car make:string model:string year:integer
```

Pull that into the db

```bash
rails db:migrate
```

### Step 1.4 Start Your App

```bash
rails server
```
