## README


This is the code for the website at bmoreonrails.org. If you'd like to help out, make a change, add a feature then come to a B'more on Rails hack night!

### Setup

* Install ruby 2.0
* `bundle install`
* `rake db:create db:migrate`
* success!

## Deployment instructions

The site is deployed to Heroku, contact a B'more on Rails organizer to be added as a collaborator to the heroku app.

## Notes

### Convert member images to square thumbnails

    for f in `ls -1 *.jpeg`; do convert -define jpeg:size=200x200 $f -thumbnail 200x200^ -gravity center -extent 200x200 app/assets/images/members/$f ; done