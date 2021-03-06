---
external help file: CosmosDB-help.xml
Module Name: CosmosDB
online version:
schema: 2.0.0
---

# Get-CosmosDbPermissionResourcePath

## SYNOPSIS

Return the resource path for a permission object.

## SYNTAX

```powershell
Get-CosmosDbPermissionResourcePath [-Database] <String> [-UserId] <String> [-Id] <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet returns the resource identifier for a
permission object.

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-CosmosDbPermissionResourcePath -Database 'MyDatabase' -UserId 'Mary' -Id 'addresses'
```

Generate a resource path for permission Id 'addresses' for user 'Mary'
in database 'MyDatabase'.

## PARAMETERS

### -Database

This is the database containing the permission.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserId

This is the Id of the user containing the permission.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

This is the Id of the permission.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.String

## NOTES

## RELATED LINKS
