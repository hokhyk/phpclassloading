# install php5.3+ versions.
# install composer
# configure the composer.json file
  
      "require": {
        "php": ">=5.4.0",
        "topthink/framework": "^5.0",
        "overtrue/wechat": "^3.2",
        "phpoffice/phpword": "^0.13.0",
        "phpoffice/phpexcel": "^1.8"
    },
	
# configure the China mirror site of packagist.com to gain quicker access to the packages:
composer config -g repo.packagist composer https://packagist.phpcomposer.com
or paste the following code in your project's composer.json file to be specific to the project only:
"repositories": {
    "packagist": {
        "type": "composer",
        "url": "https://packagist.phpcomposer.com"
    }
}

# composer install	
  If there's a composer.lock file, delete it and re-generate it using the following command:
     composer install

# in your TP5 frame's php file where you want to use PHPExcel,
  write the fllowing code to include it:
  use PHPExcel_IOFactory;
  use PHPExcel;
  
  class exportPHPExcel {
    public function exportExcelFiles ( $data = null ){
	        $phpExcel = new PHPExcel();
			...
	}
  }