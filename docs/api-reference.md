# API Reference

This document provides a high-level reference for the TaskFlow API.

## API Overview

The TaskFlow API allows applications to interact with projects, tasks, users, and task status information.

The API uses HTTP requests and returns data in JSON format.

## Base URL

~~~text
https://api.taskflow.example.com/v1
~~~

## Authentication

API requests require authentication using an API key.

Include the API key in the request header:

~~~text
Authorization: Bearer YOUR_API_KEY
~~~

Keep your API key private and do not include it in publicly shared code or documentation.

## Endpoints

### Projects

| Method | Endpoint | Description |
|---|---|---|
| GET | `/projects` | Retrieve a list of projects |
| GET | `/projects/{projectId}` | Retrieve a specific project |
| POST | `/projects` | Create a new project |
| PATCH | `/projects/{projectId}` | Update a project |
| DELETE | `/projects/{projectId}` | Delete a project |

### Tasks

| Method | Endpoint | Description |
|---|---|---|
| GET | `/projects/{projectId}/tasks` | Retrieve tasks for a project |
| GET | `/tasks/{taskId}` | Retrieve a specific task |
| POST | `/projects/{projectId}/tasks` | Create a task |
| PATCH | `/tasks/{taskId}` | Update a task |
| DELETE | `/tasks/{taskId}` | Delete a task |

## Example Request

The following example retrieves a specific project:

~~~http
GET /projects/123
Authorization: Bearer YOUR_API_KEY
~~~

## Example Response

A successful request may return a JSON response similar to:

~~~json
{
  "id": 123,
  "name": "Website Redesign",
  "description": "Tasks related to the website redesign project.",
  "status": "active"
}
~~~

## Common HTTP Methods

| Method | Purpose |
|---|---|
| GET | Retrieve information |
| POST | Create a resource |
| PATCH | Update an existing resource |
| DELETE | Remove a resource |

## Related Documentation

- [Usage Guide](usage-guide.md)
- [Workflow](workflow.md)
