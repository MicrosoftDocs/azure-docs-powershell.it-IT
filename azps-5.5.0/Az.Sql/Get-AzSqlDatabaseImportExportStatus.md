---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197726"
---
# <span data-ttu-id="344a1-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="344a1-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="344a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="344a1-102">SYNOPSIS</span></span>
<span data-ttu-id="344a1-103">Recupera i dettagli di un'importazione o esportazione di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="344a1-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="344a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="344a1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="344a1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="344a1-105">DESCRIPTION</span></span>
<span data-ttu-id="344a1-106">Il cmdlet **Get-AzSqlDatabaseImportExportStatus** ottiene i dettagli di un'importazione di file bacpac da un account di archiviazione in un database di Azure SQL o di un'esportazione di un database di Azure SQL come file bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="344a1-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="344a1-107">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="344a1-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="344a1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="344a1-108">EXAMPLES</span></span>

### <span data-ttu-id="344a1-109">Esempio 1: Ottenere lo stato di importazione ed esportazione di un database SQL</span><span class="sxs-lookup"><span data-stu-id="344a1-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="344a1-110">Questo comando ottiene lo stato di una richiesta di importazione o esportazione per un database all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="344a1-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="344a1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="344a1-111">PARAMETERS</span></span>

### <span data-ttu-id="344a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344a1-112">-DefaultProfile</span></span>
<span data-ttu-id="344a1-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="344a1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="344a1-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="344a1-114">-OperationStatusLink</span></span>
<span data-ttu-id="344a1-115">Specifica il collegamento di stato restituito dai cmdlet New-AzSqlDatabaseExport o New-AzSqlDatabaseImport stato.</span><span class="sxs-lookup"><span data-stu-id="344a1-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="344a1-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="344a1-116">-Confirm</span></span>
<span data-ttu-id="344a1-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="344a1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="344a1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344a1-118">-WhatIf</span></span>
<span data-ttu-id="344a1-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="344a1-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344a1-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="344a1-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="344a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344a1-121">CommonParameters</span></span>
<span data-ttu-id="344a1-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="344a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344a1-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="344a1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344a1-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="344a1-124">INPUTS</span></span>

### <span data-ttu-id="344a1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="344a1-125">System.String</span></span>

## <span data-ttu-id="344a1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="344a1-126">OUTPUTS</span></span>

### <span data-ttu-id="344a1-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="344a1-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="344a1-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="344a1-128">NOTES</span></span>
* <span data-ttu-id="344a1-129">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="344a1-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="344a1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="344a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="344a1-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="344a1-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="344a1-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="344a1-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="344a1-133">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="344a1-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
