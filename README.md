# generate library
nest generate library libs

# database and config module
pnpm i @nestjs/mongoose mongoose
pnpm i @nestjs/config

nest generate module database -p common 
nest generate module config -p common 

# validate env
pnpm i joi

# create a new microservice
nest g app reservations
## generate CRUD resources
nest g resource reservations
## validation and log
pnpm i class-validator class-transformer nestjs-pino pino-http pino-pretty

# generate auth app microservice
nest g app auth

## generate auth module into auth app
nest g module users
nest g controller users

