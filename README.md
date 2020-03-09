# Dango_static_config
permet de configurer les dossier static à chaque projet

# dans settings.py (a la fin) du projet
STATIC_URL = '/static/'
  MEDIA_URL = '/media/'
  STATICFILES_DIRS = [
      os.path.join(BASE_DIR,'static')
  ]
  STATIC_ROOT= os.path.join(BASE_DIR, '../static_cdn')
  MEDIA_ROOT= os.path.join(BASE_DIR, '../media_cdn')
  
  # dans urls.py du projet
  
  from django.conf import settings
  from django.conf.urls.static import static
  
  
  
  
  
  
  if settings.DEBUG :
      urlpatterns += static(settings.MEDIA_URL, document_root = settings.MEDIA_ROOT)
      urlpatterns += static(settings.STATIC_URL, document_root = settings.STATIC_ROOT) 
  
