---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176982"
---
# <span data-ttu-id="ada49-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ada49-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="ada49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada49-102">SYNOPSIS</span></span>
<span data-ttu-id="ada49-103">Ottiene un backup geo-ridondante di un database.</span><span class="sxs-lookup"><span data-stu-id="ada49-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="ada49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ada49-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada49-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ada49-105">DESCRIPTION</span></span>
<span data-ttu-id="ada49-106">Il cmdlet **Get-AzSqlDatabaseGeoBackup** ottiene un backup geo-ridondante specificato di un database SQL o di tutti i backup geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="ada49-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="ada49-107">Un backup geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica separata.</span><span class="sxs-lookup"><span data-stu-id="ada49-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="ada49-108">È possibile usare Geo-Restore per ripristinare un backup geo-ridondante in caso di un'interruzione regionale e ripristinare il database in una nuova area geografica.</span><span class="sxs-lookup"><span data-stu-id="ada49-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="ada49-109">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="ada49-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ada49-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ada49-110">EXAMPLES</span></span>

### <span data-ttu-id="ada49-111">Esempio 1: Ottenere tutti i backup geo-ridondanti in un server</span><span class="sxs-lookup"><span data-stu-id="ada49-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="ada49-112">Questo comando recupera tutti i backup geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="ada49-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="ada49-113">Esempio 2: Ottenere un backup geo-ridondante specificato</span><span class="sxs-lookup"><span data-stu-id="ada49-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="ada49-114">Questo comando recupera il backup geo-ridondante del database denominato ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="ada49-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="ada49-115">Esempio 3: Ottenere tutti i backup geo-ridondanti in un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="ada49-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="ada49-116">Questo comando recupera tutti i backup geo-ridondanti disponibili in un server specificato che inizia con "Contoso".</span><span class="sxs-lookup"><span data-stu-id="ada49-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="ada49-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada49-117">PARAMETERS</span></span>

### <span data-ttu-id="ada49-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ada49-118">-DatabaseName</span></span>
<span data-ttu-id="ada49-119">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ada49-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada49-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada49-120">-DefaultProfile</span></span>
<span data-ttu-id="ada49-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ada49-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ada49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada49-122">-ResourceGroupName</span></span>
<span data-ttu-id="ada49-123">Specifica il nome del gruppo di risorse a cui è assegnato SQL server di database locale.</span><span class="sxs-lookup"><span data-stu-id="ada49-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="ada49-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ada49-124">-ServerName</span></span>
<span data-ttu-id="ada49-125">Specifica il nome del server che ospita il backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="ada49-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="ada49-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ada49-126">-Confirm</span></span>
<span data-ttu-id="ada49-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada49-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada49-128">-WhatIf</span></span>
<span data-ttu-id="ada49-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ada49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada49-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ada49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada49-131">CommonParameters</span></span>
<span data-ttu-id="ada49-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada49-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ada49-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada49-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="ada49-134">INPUTS</span></span>

### <span data-ttu-id="ada49-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ada49-135">System.String</span></span>

## <span data-ttu-id="ada49-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ada49-136">OUTPUTS</span></span>

### <span data-ttu-id="ada49-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="ada49-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="ada49-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="ada49-138">NOTES</span></span>

## <span data-ttu-id="ada49-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ada49-139">RELATED LINKS</span></span>

[<span data-ttu-id="ada49-140">Panoramica: continuità aziendale nel cloud e ripristino di emergenza del database con SQL database</span><span class="sxs-lookup"><span data-stu-id="ada49-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="ada49-141">Recuperare un database SQL Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ada49-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="ada49-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ada49-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="ada49-143">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="ada49-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
