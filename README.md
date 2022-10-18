## file changes
- yet to be documented


<br/>

## Setup react for development
1. create a frontend directory  
`mkdir frontend && cd frontend`
2. run create-react-app command with the code institute template  
[create-react-app ci template](https://github.com/Code-Institute-Org/cra-template-moments)
3. remove the .git submodule, .gitignore and README.md  
`rm -rf .git .gitignore README.md`
4. add proxy url to package.json  
`"proxy": "http://localhost:8000"`
5. start the react development server  
`npm start`

<br/>

## Running in development
1. django will run on port 8000  
`python3 manage.py runserver`
2. react will run on port 8080  
`cd frontend && npm start`

<br/>

## Deployment

1. create a staticfiles folder in the project root directory  
`mkdir staticfiles`
2. collect admin and rest framework staticfiles  
`python3 manage.py collectstatic`
3. cd to the frontend directory and compile the react app  
`npm run build && mv build ../staticfiles/.`
 
<br/>

## Production sanity check
1. ensure all environment varaibles are set, and remote db is initialised
2. run the django server as normal, do not run the react server
3. open the gitpod preview on port 8000

<br/>

## Production Environment Variables

- SECRET_KEY
- ALLOWED_HOST
- CLIENT_ORIGIN
- DATABASE_URL
- CLOUDINARY_URL
- CLOUDINARY_SECRET
