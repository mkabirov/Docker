FROM ft-rails:on-build

EXPOSE 3000

CMD ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]



# "s" - server
# "-b" binds an IP address
# "-p" specifies port


# build & run:
#first you should run dockerfile from ft-rails!
#docker build -t ex02 .

# !!! if during building you get a mistake about rake version:
#1. go to app folder
#2. open Gemfile.lock
#3. cmd+f rake 
#4. change to the latest version (build will indicate what is needed)


#docker run -it -rm -p 3000:3000 ex02
#check on browser docker-machine ip:3000
