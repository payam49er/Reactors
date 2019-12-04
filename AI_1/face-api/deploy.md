# Examining the user interface

[Prerequisite: Detecting people with Face API](./detect-face-api.md)

With our model built, we're now ready to turn our attention to deploying our site.

## Deploy the application to Azure

With all the functionality added to our application, we're ready to publish to Azure! We will use the same [remote Git we created earlier](../computer-vision-translator/deploy.md#add-azure-as-a-remote-destination).

### Commit our changes

We need to commit our files to our repository before deployment.

``` terminal
git add app.py
git commit -m "Added facial recognition"
```

### Performing the deployment

To perform the deployment, we'll use `git push`.

``` terminal
git push azure
```

> **NOTE:** If you lost the information created in prior steps, you can display the values by using `az hack show --name <appname>` from your command or terminal window if you installed the Azure CLI, or from [Cloud Shell](https://shell.azure.com).
>
> If the username and password does not work or is not available, you can find the credentials using the Azure CLI locally if installed or on [Cloud Shell](https://shell.azure.com). `az webapp deployment user show` will display the username, and `az webapp deployment user set --user-name <username>` will allow you to set the password.

## Run the website

Now it's time to see your site in the real world! Open your browser and navigate to **https://APP_NAME.azurewebsites.net/detect**, replacing **APP_NAME** with the name of your application. Because you were training the model on Azure, you'll be able to run the detection feature without having to retrain! And, if you open the site on your mobile device you could even take a selfie to test your site.

## Summary and next steps

We've seen how to create a facial recognition application. You could enhance the site quite a bit if you'd like. You could add links to the pages (of course). You could also list the names available, and offer someone the option to either add to an existing name or create new. Maybe allow for multiple files to be uploaded? There's a lot of room to explore!
