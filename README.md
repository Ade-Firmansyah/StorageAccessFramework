# StorageAccessFramework
This Java Code For Storage access framework Android 11

## Get Permission Storage
if ((ContextCompat.checkSelfPermission(this, Manifest.permission.READ_EXTERNAL_STORAGE)  == PackageManager.PERMISSION_DENIED) && (ContextCompat.checkSelfPermission(this, Manifest.permission.WRITE_EXTERNAL_STORAGE) == PackageManager.PERMISSION_DENIED)) {
	ActivityCompat.requestPermissions(this, new String[] {Manifest.permission.READ_EXTERNAL_STORAGE, Manifest.permission.WRITE_EXTERNAL_STORAGE}, 1000);
	//Permission Denied
}
else {
	if ((ContextCompat.checkSelfPermission(this, Manifest.permission.READ_EXTERNAL_STORAGE)  == PackageManager.PERMISSION_GRANTED) && (ContextCompat.checkSelfPermission(this, Manifest.permission.WRITE_EXTERNAL_STORAGE) == PackageManager.PERMISSION_GRANTED)) {
        //Permission Granted
		intent.setClass(getApplicationContext(), MainActivity.class);
		startActivity(intent);
		finishAffinity();
	}
}
