# Installation

This page will guide you through the installation of the **Abilities** module for Game Creator.

## Creating a new project

To use abilities, first you need to install the latest version of **Game Creator**. You can find the detailed procedure by clicking on the [documentation link](https://docs.gamecreator.io/gamecreator/getting-started/installation/).


Get the **Abilities** package from the Unity Asset Store following the link below:

[Get Abilities :fontawesome-brands-unity: ](https://assetstore.unity.com/packages/slug/206589){ .md-button .md-button--primary }

Once you have purchased it, click on the *Import* button on the website and the Unity Editor's Package Manager window should appear with the **Ability** package selected. Click on Download and Import afterwards.

Before going further, please make sure that you have downloaded and installed **UniRX**, a free library extension for Unity. You can find it in the asset store at the following link.

[Get UniRX :fontawesome-brands-unity: ](https://assetstore.unity.com/packages/tools/integration/unirx-reactive-extensions-for-unity-17276){ .md-button .md-button--primary }

Once this process completed, you will have a new "Game Creator" menu at the top-toolbar. Open it the menu and click on *Install...* The following window will open.

<figure markdown>
  ![Image title](https://github.com/daimahou/documentation/blob/main/docs/img/install.png?raw=true){ width="600" }
  <figcaption>Install window - Core</figcaption>
</figure>

Select **Abilities** in the menu tree, and then click on *Install x.y.z* button. This will automatically install all the necessary packages.

Let the process complete and if everything went fine, your console shouldn't have any errors. If you do, please feel free to reach out to our [support email](mailto:daimahou.studio@gmail.com).

!!! tip "Using Git ? Add the following lines to your .gitignore file"
    
    ``` # Daimahou Games``` 

    ``` /Assets/Plugins/DaimahouGames/Packages``` 

## Examples

After the successful installation of both **Game Creator** and **Abilities**, another menu will appear in the Installation window. This menu will provide with additional content in the form of *examples* to get you familiar with the different concepts that makes up **Abilities**.


For more information on how to install *examples*, please refer to the [following link](https://docs.gamecreator.io/gamecreator/getting-started/examples/).


Once installed, the example will appear under ```Assets/Plugins/GameCreator/Installs/``` or you can simply click the Select button to automatically select the example's folder.

<figure markdown>
  ![Image title](https://github.com/daimahou/documentation/blob/main/docs/img/install-examples.png?raw=true){ width="600" }
  <figcaption>Install window - Examples</figcaption>
</figure>

!!! danger "Uninstallation"

    Although examples can be uninstall by simply clicking the Uninstall button. To uninstall Abilities and the Core module of Daimahou, simply pressing the uninstall button will NOT be enough. AFTER pressing uninstall, please delete the following folder :

    ``` /Assets/Plugins/DaimahouGames/Packages ```

