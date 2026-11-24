# scoop-bucket

A personal [Scoop](https://scoop.sh) bucket by [@rifatno1](https://github.com/rifatno1).

Manifests in this bucket are checked for new versions automatically once a day and updated by a GitHub Actions workflow.

## Prerequisites

You need Scoop installed. If you don't have it yet, open PowerShell and run:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
```

`git` is also required to add buckets:

```powershell
scoop install git
```

## Add this bucket

```powershell
scoop bucket add rifatno1 https://github.com/rifatno1/scoop-bucket
```

Check that it was added:

```powershell
scoop bucket list
```

## Install a package

```powershell
scoop install rifatno1/<package-name>
```

For example:

```powershell
scoop install rifatno1/example-app
```

The `rifatno1/` prefix is optional if no other bucket has a package with the same name:

```powershell
scoop install <package-name>
```

## Browse available packages

List or search the packages in this bucket:

```powershell
scoop search rifatno1
scoop search <keyword>
```

Or look in the [`bucket`](bucket) folder of this repository.

## Update

Refresh the bucket and update installed packages:

```powershell
scoop update          # fetch the latest manifests
scoop update <package-name>
scoop update *        # update everything installed
```

## Uninstall

```powershell
scoop uninstall <package-name>
```

To remove the bucket entirely:

```powershell
scoop bucket rm rifatno1
```

## Contributing

Found an outdated or broken package? [Open an issue](https://github.com/rifatno1/scoop-bucket/issues) or submit a pull request.
