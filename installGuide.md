# Step 1: #

checkout the source code (requires subversion):
```
    svn checkout http://django-profiling.googlecode.com/svn/trunk/ django-profiling
```

# Step 2: #

copy the "profiling" directory into your python path

# Step 3: #

Add "profiling" to the INSTALLED\_APPS section of your settings.py file

# Step 4: #

Add this to the end of your MIDDLEWARE\_CLASSES section of your settings.py file
```
    'profiling.middleware.ProfileMiddleware',
```

# Step 5: #

do a syncdb to add the database tables:
```
    python manage.py syncdb
```

# Step 6: #

Visit any url in your django site that you want to profile... for example:
```
    http://example.com/blog/
```

to view profiling information add "prof" to the url as a get request like so:
```
    http://example.com/blog/?prof
```

You should see profiling info =D