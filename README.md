# CI-Slugify

CodeIgniter Slug Generator Library

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FWebFikirleri%2FCI-Slugify&count_bg=%233D8FC8&title_bg=%23555555&icon=microsoftacademic.svg&icon_color=%23E7E7E7&title=VISITS&edge_flat=true)](https://hits.seeyoufarm.com)

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
    
It generates a new unique slug. If same slug exists, it will append a numeric value to the slug. Ex:

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
