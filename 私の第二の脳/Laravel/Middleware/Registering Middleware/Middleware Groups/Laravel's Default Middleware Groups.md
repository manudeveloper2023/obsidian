Laravel incluye grupos de **`middleware`** predefinidas para ``web`` y `api` que contienen `middlewares comunes` que podrias querer aplicarlos en tu `web` o `rutas de API`.Los aplica correspondiendo si son `web` o `api`

|The `web` Middleware Group|
|---|
|`Illuminate\Cookie\Middleware\EncryptCookies`|
|`Illuminate\Cookie\Middleware\AddQueuedCookiesToResponse`|
|`Illuminate\Session\Middleware\StartSession`|
|`Illuminate\View\Middleware\ShareErrorsFromSession`|
|`Illuminate\Foundation\Http\Middleware\ValidateCsrfToken`|
|`Illuminate\Routing\Middleware\SubstituteBindings`|

| The `api` Middleware Group                         |
| -------------------------------------------------- |
| `Illuminate\Routing\Middleware\SubstituteBindings` |
## Tags

##### #Laravel