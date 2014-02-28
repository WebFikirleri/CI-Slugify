# CI-Slugify

CodeIgniter Slug Generator Library

## Usage

### Loading library:

    $this->load->library('slugify');

### Convert a text to slug:
    
    $text = 'This text will be slug!';
    $slug = $this->slugify->slug($text);
    echo $slug;
    
### Create a unique slug:

#### Inserting a record

    $title = 'Page Title which is going to be a slug';
    $slug = $this->slugify->slug_unique($title, 'posts_table', 'slug');
    
It generates a new unique slug. If same slug exists it appends a numeric value to slug. Ex:

* about-us
* about-us-1
* about-us-2
* ...
* about-us-999
* etc...

#### Updating Record

    $post_id = 10;
    $title = 'Page Title which is going to be a slug';
    $slug = $this->slugify->slug_unique($title, 'posts_table', 'slug', $post_id);
    
It generates a new unique slug. It excludes from self row...
