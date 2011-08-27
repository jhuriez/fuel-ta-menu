# TA-Menu

FuelPHP Package to generate recursively nested menu's from multiple sources. Currently we only have a database source (one table) however feel free to fork or add your own sources.

### Example Usage

	<ul><?=\TA\Menu::render('menu_items')?></ul>
	// menu_items is the table name
	
### Install

Add `http://github.com/tarnfeld` to your packages config and run `php oil install ta-menu`. Dont forget to include the package in your config.

### Sample DB Structure

    CREATE TABLE `menu_items` (
	  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
	  `parent_id` int(11) DEFAULT NULL,
	  `title` varchar(255) DEFAULT NULL,
	  `link` text,
	  `position` int(11) DEFAULT NULL,
	  PRIMARY KEY (`id`)
	) ENGINE=InnoDB AUTO_INCREMENT=8 DEFAULT CHARSET=latin1;