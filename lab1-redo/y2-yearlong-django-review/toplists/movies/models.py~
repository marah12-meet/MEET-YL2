from django.db import models

class Movie(models.Model):
    # you must always remember to specify a max_length 
    # for CharFields
    title = models.CharField(max_length=500)

    # this method is used to determine how the model 
    # will be displayed in the shell (in this case, 
    # instead of printing something like Movie<1245315>
    # it will print Movie<Shrek> or whatever the title is)
    def __unicode__(self):
        return self.title

class Comment(models.Model):
    text = models.CharField(max_length=1000)
    # why does this have a ForeignKey relationship with
    # a movie? Because every comment is associated with
    # exactly one movie
    movie = models.ForeignKey(Movie)

    def __unicode__(self):
        return self.movie.title + ": " + self.text