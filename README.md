# generate library
nest generate library my-lib

# database and config module
pnpm i @nestjs/mongoose mongoose
pnpm i @nestjs/config

nest generate module database -p common 
nest generate module config -p common 

# validate env
pnpm i joi