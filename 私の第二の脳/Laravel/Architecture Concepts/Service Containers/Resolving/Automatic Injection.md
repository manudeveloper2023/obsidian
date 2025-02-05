```php
<?php
 
namespace App\Http\Controllers;
 
use App\Services\AppleMusic;
 
class PodcastController extends Controller
{
    /**
     * Create a new controller instance.
     */
    public function __construct(
        protected AppleMusic $apple,
    ) {}
 
    /**
     * Show information about the given podcast.
     */
    public function show(string $id): Podcast
    {
        return $this->apple->findPodcast($id);
    }
}
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers