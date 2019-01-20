# unity-zxing

This is a unity-only rebundle of https://github.com/micjahn/ZXing.Net

It packages version `0.16.2`, because version `0.16.4+` are broken for unity.

The examples in `Demo` are from `https://github.com/linmq/ZXing_Unity3D_Test`.

See that project for usage details.

## Install

From your unity project folder:

    npm init
    npm install shadowmint/unity-zxing --save
    echo Assets/pkg-all >> .gitignore
    echo Assets/pkg-all.meta >> .gitignore

The package and all its dependencies will be installed in
your Assets/pkg-all folder.

You may need to add these compile constants under Edit > Project Settings > Player > Other Settings

    NET35,UNITY,WINDOWS_PHONE

## Development

Setup and run tests:

    cd test
    npm install

Remember that changes made to the test folder are not saved to the package
unless they are copied back into the source folder.

To reinstall the files from the src folder, run `npm install ..` again.

## Sync from origin

    git clone https://github.com/micjahn/ZXing.Net.git origin --depth 1
    open origin/Source/lib/zxing.unity.csproj
    rm -rf src/ZXing.Net

Now copy all the files over into src/ZXing.Net
