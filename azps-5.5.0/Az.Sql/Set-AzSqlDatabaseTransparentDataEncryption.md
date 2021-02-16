---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178351"
---
# <span data-ttu-id="3dc4e-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3dc4e-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="3dc4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc4e-103">Modifica la proprietà TDE di un database.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="3dc4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc4e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc4e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3dc4e-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc4e-106">Il cmdlet **Set-AzSqlDatabaseTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (TDE) di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="3dc4e-107">Per altre informazioni, vedere Transparent Data Encryption con Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( nella Microsoft Developer Network https://msdn.microsoft.com/library/dn948096) Library.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="3dc4e-108">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3dc4e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc4e-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc4e-110">Esempio 1: Abilitare TDE per un database</span><span class="sxs-lookup"><span data-stu-id="3dc4e-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="3dc4e-111">Questo comando abilita TDE per il database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="3dc4e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dc4e-112">PARAMETERS</span></span>

### <span data-ttu-id="3dc4e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3dc4e-113">-DatabaseName</span></span>
<span data-ttu-id="3dc4e-114">Specifica il nome del database modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-114">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc4e-115">-DefaultProfile</span></span>
<span data-ttu-id="3dc4e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3dc4e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="3dc4e-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3dc4e-119">-ServerName</span></span>
<span data-ttu-id="3dc4e-120">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-120">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-121">-State</span><span class="sxs-lookup"><span data-stu-id="3dc4e-121">-State</span></span>
<span data-ttu-id="3dc4e-122">Specifica il valore della proprietà TDE.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="3dc4e-123">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3dc4e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dc4e-124">Abilitato</span><span class="sxs-lookup"><span data-stu-id="3dc4e-124">Enabled</span></span> 
- <span data-ttu-id="3dc4e-125">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="3dc4e-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dc4e-126">-Confirm</span></span>
<span data-ttu-id="3dc4e-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc4e-128">-WhatIf</span></span>
<span data-ttu-id="3dc4e-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc4e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc4e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc4e-131">CommonParameters</span></span>
<span data-ttu-id="3dc4e-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc4e-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3dc4e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc4e-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="3dc4e-134">INPUTS</span></span>

### <span data-ttu-id="3dc4e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="3dc4e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="3dc4e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3dc4e-136">System.String</span></span>

## <span data-ttu-id="3dc4e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc4e-137">OUTPUTS</span></span>

### <span data-ttu-id="3dc4e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="3dc4e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="3dc4e-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="3dc4e-139">NOTES</span></span>

## <span data-ttu-id="3dc4e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc4e-140">RELATED LINKS</span></span>

[<span data-ttu-id="3dc4e-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3dc4e-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="3dc4e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="3dc4e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="3dc4e-143">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="3dc4e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


