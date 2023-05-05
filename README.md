# Stanbridge Fullstack Developer Challenge

This is a mono-repo containing the code for the backend and frontend of the Stanbridge Fullstack Developer Challenge.

## Overview
For a single course titled “Example Course,” display a roster of students to an instructor
allowing the instructor to record each student as present or absent. Use the example
student data provided on page 2 of this document to populate the roster.

## Requirements
1. Backend built in Laravel
2. Frontend built in Vue
3. Frontend must interact with backend via RESTful API
4. Backend must persist present/absent status in a MySQL database
5. Write at least one feature or unit test in PHPUnit

## Backend

The backend is a REST API written in Laravel 10. It is meant to be simple, just lists courses, students with their attendance status by date and course, and allows for the updated of the attendance status.

### API Endpoints

- `GET /api/courses` - List all courses
- `GET /api/courses/{course}/students` - List all students in a course with their attendance status
- `POST /api/attendances` - Update the attendance status of a student

### Running the backend

It's a standard Laravel application, so you can run it with `php artisan serve` after installing the dependencies with `composer install`.

#### Install dependencies

```bash
composer install
```

#### Run the server

```bash
php artisan serve
```

This will start the server on `http://localhost:8000` by default.

#### Run the tests

```bash
php artisan test
```

## Frontend

The frontend is a Vue 3 application written in TypeScript. It uses the Vite build tool and the Vue Router library and Pinia for state management.

### Running the frontend

#### Install dependencies

```bash
yarn
```

#### Run the server

```bash
yarn dev
```

This will start the server on `http://localhost:5173` by default.

#### Tests
This project doesn't have any tests as per the requirements of the challenge.


## Considerations

This repo has both the backend and frontend in the same repo as git submodules for an easier way of sharing them together.

Each submodule has the default documentation for each framework.