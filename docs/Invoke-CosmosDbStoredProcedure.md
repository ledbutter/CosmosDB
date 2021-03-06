---
external help file: CosmosDB-help.xml
Module Name: CosmosDB
online version:
schema: 2.0.0
---

# Invoke-CosmosDbStoredProcedure

## SYNOPSIS

Execute a new stored procedure for a collection in a Cosmos DB database.

## SYNTAX

### Context (Default)

```powershell
Invoke-CosmosDbStoredProcedure -Context <Context> [-KeyType <String>] [-Key <SecureString>]
 [-Database <String>] -CollectionId <String> [-PartitionKey <String[]>] -Id <String>
 [-StoredProcedureParameter <Object[]>] [<CommonParameters>]
```

### Account

```powershell
Invoke-CosmosDbStoredProcedure -Account <String> [-KeyType <String>] [-Key <SecureString>]
  [-Database <String>] -CollectionId <String> [-PartitionKey <String[]>] -Id <String>
  [-StoredProcedureParameter <Object[]>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will execute a stored procedure contained in a collection
in a Cosmos DB.

## EXAMPLES

### Example 1

```powershell
PS C:\> Invoke-CosmosDbStoredProcedure -Context $cosmosDbContext -CollectionId 'MyNewCollection' -Id 'spHelloWorld'
```

Execute a stored procedure called 'spHelloWorld' in a collection in the
database.

### Example 2

```powershell
PS C:\> Invoke-CosmosDbStoredProcedure -Context $cosmosDbContext -CollectionId 'MyNewCollection' -Id 'spHelloWorld' -StoredProcedureParameters @('PowerShell')
```

Execute a stored procedure called 'spHelloWorld' passing in the parameter
'PowerShell' in a collection in the database.

## PARAMETERS

### -Context

This is an object containing the context information of the Cosmos DB database
that will be deleted. It should be created by \`New-CosmosDbContext\`.

```yaml
Type: Context
Parameter Sets: Context
Aliases: Connection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Account

The account name of the Cosmos DB to access.

```yaml
Type: String
Parameter Sets: Account
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType

The type of key that will be used to access ths Cosmos DB.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Master
Accept pipeline input: False
Accept wildcard characters: False
```

### -Key

The key to be used to access this Cosmos DB.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

The name of the database to access in the Cosmos DB account.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

This is the Id of the collection that contains the stored procedure
to execute.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKey

This is the Partition Keys of the collection that contains the stored
procedure to execute.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

This is the Id of the stored procedure to execute.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StoredProcedureParameter

This is an array of strings that will be passed as stored
procedure parameters.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
