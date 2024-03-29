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
### passport 
pnpm i @nestjs/passport passport passport-local
pnpm i -D @types/passport-local
### jwt
pnpm i @nestjs/jwt passport-jwt
pnpm i -D @types/passport-jwt

#### add bcrypt to encrypt password
pnpm i bcryptjs
pnpm i -D @types/bcryptjs

#### parse cookie
pnpm i cookie-parser
pnpm i -D @types/cookie-parser

# add microservice to app
pnpm i @nestjs/microservices

