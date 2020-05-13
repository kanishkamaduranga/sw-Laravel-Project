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
 REQUEST :    curl --location --request GET 'http://127.0.0.1:8001/api/v1/organization?page=3&limit=10'
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
<pre>
REQUEST :-    curl --location --request GET 'http://127.0.0.1:8001/api/v1/user?page=3&limit=10'
</pre>
<pre>
RESPONSE :- 
"status": 200,
    "description": "OK",
    "data": {
        "current_page": 3,
        "data": {
            "20": {
                "_id": 21,
                "url": "http://initech.tokoin.io.com/api/v2/users/21.json",
                "external_id": "b4524a24-212a-4ce5-ba6b-c488b72a3ad5",
                "name": "Leon Oneil",
                "alias": "Miss Dee",
                "created_at": "2016-03-01T03:12:09 -11:00",
                "active": true,
                "verified": false,
                "shared": true,
                "locale": "de-CH",
                "timezone": "Bosnia and Herzegovina",
                "last_login_at": "2014-12-10T06:19:41 -11:00",
                "email": "deeoneil@flotonic.com",
                "phone": "9314-713-633",
                "signature": "Don't Worry Be Happy!",
                "organization_id": 110,
                "tags": [
                    "Faxon",
                    "Bellfountain",
                    "Gracey",
                    "Muir"
                ],
                "suspended": false,
                "role": "admin"
            },
            
            .................................
        },
        "from": 21,
        "to": 30,
        "last_page": 8,
        "pre_page": 10,
        "total": 75
    }
}
</pre>

- GET Tickets
<pre>
REQUEST :-     curl --location --request GET 'http://127.0.0.1:8001/api/v1/ticket?page=10&limit=10'
</pre>
<pre>
RESPONSE :-  

{
    "status": 200,
    "description": "OK",
    "data": {
        "current_page": 10,
        "data": {
            "90": {
                "_id": "6e77bbf1-5fc7-4f41-aeb1-74f8730f974b",
                "url": "http://initech.tokoin.io.com/api/v2/tickets/6e77bbf1-5fc7-4f41-aeb1-74f8730f974b.json",
                "external_id": "3ce8b7f5-952b-485a-a6c3-8d5259d3850a",
                "created_at": "2016-06-24T07:57:38 -10:00",
                "type": "problem",
                "subject": "A Problem in Guatemala",
                "description": "Ex labore dolor commodo magna ex pariatur sunt amet ad quis duis laborum. Fugiat anim non esse eu sunt elit.",
                "priority": "high",
                "status": "open",
                "submitter_id": 49,
                "assignee_id": 26,
                "organization_id": 119,
                "tags": [
                    "Texas",
                    "Nevada",
                    "Oregon",
                    "Arizona"
                ],
                "has_incidents": true,
                "due_at": "2016-08-01T11:20:58 -10:00",
                "via": "voice"
            },
            
            .................................................
        },
        "from": 91,
        "to": 100,
        "last_page": 20,
        "pre_page": 10,
        "total": 200
    }
}
</pre>
