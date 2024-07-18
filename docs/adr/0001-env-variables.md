# 1. env-variables

Date: 2024-07-16

## Status

2024-07-16 proposed

## Context

The application currently uses a json file to store the path and requires this path
to be set before the application will start. Currently the only thing stored in the 
json config is the path, so there's some overhead in parsing the file before the 
application launches.

## Decision

Switch to using environment variables instead of json and remove the requirement for the path
to be set in order for the application to start.

## Consequences

All the code related to loading the json file will need to be removed. Not requiring the path 
to media to be set up beforehand will allow the user to select a path in the app instead of 
editing the config file before startup.
