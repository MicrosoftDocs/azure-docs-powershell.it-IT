---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 218af86b3cdc97ecbfccb07e54a57646ab5ff414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999694"
---
# <span data-ttu-id="92a26-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="92a26-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="92a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a26-102">SYNOPSIS</span></span>
<span data-ttu-id="92a26-103">Recupera i dettagli di un'importazione o esportazione di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="92a26-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="92a26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92a26-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a26-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92a26-105">DESCRIPTION</span></span>
<span data-ttu-id="92a26-106">Il cmdlet **Get-AzSqlDatabaseImportExportStatus** ottiene i dettagli di un'importazione di file bacpac da un account di archiviazione in un database di Azure SQL o di un'esportazione di un database di Azure SQL come file bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92a26-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="92a26-107">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="92a26-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="92a26-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92a26-108">EXAMPLES</span></span>

### <span data-ttu-id="92a26-109">Esempio 1: Ottenere lo stato di importazione ed esportazione di un database SQL</span><span class="sxs-lookup"><span data-stu-id="92a26-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="92a26-110">Questo comando ottiene lo stato di una richiesta di importazione o esportazione per un database all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="92a26-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="92a26-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92a26-111">PARAMETERS</span></span>

### <span data-ttu-id="92a26-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a26-112">-DefaultProfile</span></span>
<span data-ttu-id="92a26-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="92a26-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92a26-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="92a26-114">-OperationStatusLink</span></span>
<span data-ttu-id="92a26-115">Specifica il collegamento di stato restituito dai cmdlet New-AzSqlDatabaseExport o New-AzSqlDatabaseImport stato.</span><span class="sxs-lookup"><span data-stu-id="92a26-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="92a26-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92a26-116">-Confirm</span></span>
<span data-ttu-id="92a26-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a26-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a26-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a26-118">-WhatIf</span></span>
<span data-ttu-id="92a26-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a26-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a26-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a26-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a26-121">CommonParameters</span></span>
<span data-ttu-id="92a26-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a26-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92a26-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a26-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="92a26-124">INPUTS</span></span>

### <span data-ttu-id="92a26-125">System.String</span><span class="sxs-lookup"><span data-stu-id="92a26-125">System.String</span></span>

## <span data-ttu-id="92a26-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92a26-126">OUTPUTS</span></span>

### <span data-ttu-id="92a26-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="92a26-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="92a26-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="92a26-128">NOTES</span></span>
* <span data-ttu-id="92a26-129">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="92a26-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="92a26-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92a26-130">RELATED LINKS</span></span>

[<span data-ttu-id="92a26-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="92a26-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="92a26-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="92a26-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="92a26-133">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="92a26-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
