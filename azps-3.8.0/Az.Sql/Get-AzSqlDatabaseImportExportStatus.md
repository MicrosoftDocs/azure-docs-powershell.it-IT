---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019505"
---
# <span data-ttu-id="2503f-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="2503f-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="2503f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2503f-102">SYNOPSIS</span></span>
<span data-ttu-id="2503f-103">Ottiene i dettagli di un'importazione o esportazione di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2503f-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="2503f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2503f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2503f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2503f-105">DESCRIPTION</span></span>
<span data-ttu-id="2503f-106">Il cmdlet **Get-AzSqlDatabaseImportExportStatus** ottiene i dettagli di un'importazione di file di BACPAC da un account di archiviazione a un database SQL di Azure o un'esportazione di un database SQL di Azure come file di BACPAC in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2503f-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="2503f-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="2503f-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2503f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2503f-108">EXAMPLES</span></span>

### <span data-ttu-id="2503f-109">Esempio 1: ottenere lo stato di importazione ed esportazione di un database SQL</span><span class="sxs-lookup"><span data-stu-id="2503f-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="2503f-110">Questo comando ottiene lo stato di una richiesta di importazione o esportazione per un database in corrispondenza dell'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="2503f-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="2503f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2503f-111">PARAMETERS</span></span>

### <span data-ttu-id="2503f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2503f-112">-DefaultProfile</span></span>
<span data-ttu-id="2503f-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2503f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2503f-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="2503f-114">-OperationStatusLink</span></span>
<span data-ttu-id="2503f-115">Specifica il collegamento di stato restituito dai cmdlet New-AzSqlDatabaseExport o New-AzSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="2503f-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="2503f-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2503f-116">-Confirm</span></span>
<span data-ttu-id="2503f-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2503f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2503f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2503f-118">-WhatIf</span></span>
<span data-ttu-id="2503f-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2503f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2503f-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2503f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2503f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2503f-121">CommonParameters</span></span>
<span data-ttu-id="2503f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2503f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2503f-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2503f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2503f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2503f-124">INPUTS</span></span>

### <span data-ttu-id="2503f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2503f-125">System.String</span></span>

## <span data-ttu-id="2503f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2503f-126">OUTPUTS</span></span>

### <span data-ttu-id="2503f-127">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="2503f-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="2503f-128">Note</span><span class="sxs-lookup"><span data-stu-id="2503f-128">NOTES</span></span>
* <span data-ttu-id="2503f-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2503f-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="2503f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2503f-130">RELATED LINKS</span></span>

[<span data-ttu-id="2503f-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="2503f-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="2503f-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="2503f-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="2503f-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2503f-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
