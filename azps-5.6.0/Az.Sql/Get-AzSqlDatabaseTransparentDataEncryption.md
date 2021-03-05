---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 1b045b97df1dbbc704f3288cf2075caa16f30bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014718"
---
# <span data-ttu-id="d6850-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d6850-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="d6850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6850-102">SYNOPSIS</span></span>
<span data-ttu-id="d6850-103">Ottiene lo stato TDE per un database.</span><span class="sxs-lookup"><span data-stu-id="d6850-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="d6850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6850-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6850-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6850-105">DESCRIPTION</span></span>
<span data-ttu-id="d6850-106">Il cmdlet **Get-AzSqlDatabaseTransparentDataEncryption** ottiene lo stato di Transparent Data Encryption (TDE) per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d6850-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="d6850-107">Per altre informazioni, vedere Transparent Data Encryption con Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( nella Microsoft Developer Network https://msdn.microsoft.com/library/dn948096) Library.</span><span class="sxs-lookup"><span data-stu-id="d6850-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="d6850-108">Questo cmdlet ottiene lo stato corrente di TDE, ma sia la crittografia che la decrittografia possono essere operazioni a esecuzione lunga.</span><span class="sxs-lookup"><span data-stu-id="d6850-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="d6850-109">Per visualizzare lo stato dell'analisi della crittografia, eseguire il cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity crittografia.</span><span class="sxs-lookup"><span data-stu-id="d6850-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="d6850-110">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="d6850-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d6850-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6850-111">EXAMPLES</span></span>

### <span data-ttu-id="d6850-112">Esempio 1: Ottenere lo stato TDE per un database</span><span class="sxs-lookup"><span data-stu-id="d6850-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="d6850-113">Questo comando ottiene lo stato di TDE per il database denominato Database01 nel server denominato server01.</span><span class="sxs-lookup"><span data-stu-id="d6850-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="d6850-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6850-114">PARAMETERS</span></span>

### <span data-ttu-id="d6850-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6850-115">-DatabaseName</span></span>
<span data-ttu-id="d6850-116">Specifica il nome del database per cui questo cmdlet ottiene lo stato TDE.</span><span class="sxs-lookup"><span data-stu-id="d6850-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="d6850-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6850-117">-DefaultProfile</span></span>
<span data-ttu-id="d6850-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6850-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6850-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6850-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6850-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="d6850-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d6850-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6850-121">-ServerName</span></span>
<span data-ttu-id="d6850-122">Specifica il nome del server che ospita il database per cui questo cmdlet ottiene lo stato TDE.</span><span class="sxs-lookup"><span data-stu-id="d6850-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="d6850-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6850-123">-Confirm</span></span>
<span data-ttu-id="d6850-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6850-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6850-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6850-125">-WhatIf</span></span>
<span data-ttu-id="d6850-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6850-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6850-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6850-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6850-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6850-128">CommonParameters</span></span>
<span data-ttu-id="d6850-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6850-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6850-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6850-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6850-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6850-131">INPUTS</span></span>

### <span data-ttu-id="d6850-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d6850-132">System.String</span></span>

## <span data-ttu-id="d6850-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6850-133">OUTPUTS</span></span>

### <span data-ttu-id="d6850-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="d6850-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="d6850-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6850-135">NOTES</span></span>

## <span data-ttu-id="d6850-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6850-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6850-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="d6850-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="d6850-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d6850-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
