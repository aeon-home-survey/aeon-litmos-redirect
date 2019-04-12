# aeon-litmos-redirect
Custom JS for a redirect on Aeon's instance of Litmos

# requirements
"Team lead" user role should be directed to `/home/dashboard` on login instead of the app's default `/admin/dashboard` landing page

# implementation
When going to `/home/dashboard`, if all of the following are true, the user is redirected to `/admin/dashboard`:
* "Account Settings" element unavailable in nav dropdown (aka user is not "Admin" role)
* Referrer is not an `aeon.litmos.com` page
* Page being loaded is `/home/dashboard`

# deployment
As a Litmos admin, go to `https://aeon.litmos.com/settings/theme` and add the contents of `custom.html` to the **Custom Javascript** field.