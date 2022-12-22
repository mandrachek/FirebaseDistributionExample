Example project showing how firebase app distribution plugin doesn't work right.
After checking out the project you will need to:

1) Setup a firebase project with android apps configured for:
- com.andrachek.myapplication
- com.andrachek.myapplication.debug
- com.andrachek.myapplication.dev
- com.andrachek.myapplication.dev.debug
- com.andrachek.myapplication.qa
- com.andrachek.myapplication.qa.debug
- com.andrachek.myapplication.staging
- com.andrachek.myapplication.staging.debug
 
2) Download the `google-services.json` and copy it to the `app/` folder.

3) Get your firebase service account credentials json, and place it in `config/` folder as `distribution-credentials.json`.

4) Copy your ~/.android/debug.keystore into config/keys

5) Run `./gradlew assembleDevDebug appDistributionUploadDevDebug`