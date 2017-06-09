# Classification_OMTD 

## Run standalone

`cat input.xml | python madis/src/mexec.py -f  PATH/classify.sql -d PATH/taxonomies.db > output.json`

## Docker
### Build 
`docker build -t <name>`

### Run 
`docker run -it -v <host-dir>:/usr/app/src/data --rm --name <name> <name>`

Remember to declare <host-dir> with an absolute path, for example `${PWD}/` or `/home/user/data`.

- For example
`docker run -it -v $PWD/<xml_files>:/usr/app/src/data --rm --name <name> <name>`

### Results 
The docker images expects an `xml` file inside the folder and writes the result in a `results.json` file that is saved in the host
s filesystem.
