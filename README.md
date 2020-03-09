# Dango_static_config
permet de configurer les dossier static à chaque projet

dans settings.py du projet

STATIC_URL = '/static/'
  MEDIA_URL = '/media/'
  STATICFILES_DIRS = [
      os.path.join(BASE_DIR,'static')
  ]
  STATIC_ROOT= os.path.join(BASE_DIR, '../static_cdn')
  MEDIA_ROOT= os.path.join(BASE_DIR, '../media_cdn')
