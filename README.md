# Django Models

## Class-27

---

<br>

### Feature Tasks and Requirements
<br>

- <b>Model</b>
    - create snack_tracker_project project
        - This will involve some preliminary steps.
        - Review previous class lab for details.

    <br>

    - create snacks app

    <br>

    - Add snacks app to project

    <br>

    - create Snack mode

        - make sure it extends from proper base class
        - add name as a CharField with maximum length of 64 characters.
        - add purchaser ForeignKey related to Django’s built in user model with CASCADE delete option
            - from django.contrib.auth import get_user_model
        - add description TextField

    <br>

    - add model to admin
        
    <br>

    - modify Snack model have user friendly display in admin

    <br>

    - create migrations and migrate data

    <br>

    - create a super user

    <br>

    - run development server

    <br>

    - Add a few snacks via Admin panel

    <br>

    - create another user and more snacks via Admin panel

    <br>

    - confirm that snacks behave as expected with proper name, purchaser and description.

    <br>

    - Looks like your model in good shape. Congrats!

<br>
<br>
<br>

- <b>Views for Snacks App</b>
    - Where to create these views?
        - Dig around and see if there’s a sensible spot.
        - HINT There is one correct place for your app’s views.

    <br>

    - create SnackListView
        - extend ListView
        - give a template of snack_list.html
        - associate Snack mode
    
    <br>

    - update url patterns for project
        - empty path should include snacks.urls

    <br>

    - update snacks app urls
        - empty sub-path should be handled by SnackListView
            - Don’t forget to use as_view()

    <br>

    - add detail view
        - link snack_detail.html template
        - associate Snack model

    <br>

    - update app urlpatterns to handle detail view
        - account for primary key in url
        - path would look like localhost:8000/1/ to get to snack with id of 1

<br>
<br>
<br>

- <b>Templates</b>
    - Addtemplates folder in root of project
        - register templates folder in project settings TEMPLATES section

    <br>

    - create base.html ancestor template
        - add main html document
        - use Django Templating Language to allow child templates to insert content

    <br>

    - create snack_list.html template
        - extend base template
        - use Django Templating Language to display each snack’s name

    <br>

    - view home page (aka snack_list) and confirm snacks showing properly

    <br>

    - create snack_detail.html template
        - template should extend base
        - content should display snack’s name, description and purchaser

    <br>

    - add link in snack_list template to related detail page for each snack

    <br>

    - Add a link back to Home (aka snack_list) page from detail page.

<br>
<br>
<br>

- <b>User Acceptance Tests</b>
    - Test Snack pages
        - NOTE make sure test extends TestCase instead of SimpleTestCase used in previous class.
        - verify status code
        - verify correct template use
        - use url name instead of hard coded path
            - TIP: django.urls.reverse will help with that.

    <br>

    - We can’t easily test SnackDetailView just yet.
        - Can you figure out why?

<br>
<br>
<br>

- <b>Configuration</b>
    - Create django-models GitHub repository.
    - Create a virtual environment inside django-models.

<br>
<br>

---

<br>

**- Esmail Jawabreh**