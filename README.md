# swivel

#this is Swivel test 


# Getting started

## Installation

Clone the repository
git clone https://github.com/kanishkamaduranga/swivel.git 

Switch to the repo folder

nstall all the dependencies using composer

    composer install

Copy the example env file and make the required configuration changes in the .env file

    cp .env.example .env

Generate a new application key

    php artisan key:generate

Start the local development server

    php artisan serve

You can now access the server at http://localhost:8000

## Setup Postman Collection

 "swivel.postman_collection.json" and "swivel-local.postman_environment.json" files are import to post man
 
double check postman evoronment with serve url 
 
 
## Start Testing

- GET Organization
<pre>
 rEQUEST :    curl --location --request GET 'http://127.0.0.1:8001/api/v1/organization?page=3&limit=10'
</pre>
<pre>
RESPONSE :-   {
    "status": 200,
    "description": "OK",
    "data": {
        "current_page": 3,
        "data": {
            "20": {
                "_id": 121,
                "url": "http://initech.tokoin.io.com/api/v2/organizations/121.json",
                "external_id": "3fffbf20-9172-4d1d-923b-f247d9132e3a",
                "name": "Hotcâkes",
                "domain_names": [
                    "recrisys.com",
                    "qiao.com",
                    "makingway.com",
                    "shopabout.com"
                ],
                "created_at": "2016-01-02T06:07:59 -11:00",
                "details": "MegaCorp",
                "shared_tickets": true,
                "tags": [
                    "Howard",
                    "Moreno",
                    "Benton",
                    "Bonner"
                ]
            },
            .............................
        },
        "from": 21,
        "to": 25,
        "last_page": 3,
        "pre_page": 10,
        "total": 25
    }
}
</pre>

- GET Users
