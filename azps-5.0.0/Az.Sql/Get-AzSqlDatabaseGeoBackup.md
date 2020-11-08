---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203064"
---
# <span data-ttu-id="07377-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="07377-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="07377-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07377-102">SYNOPSIS</span></span>
<span data-ttu-id="07377-103">Ottiene un backup Geo-ridondante di un database.</span><span class="sxs-lookup"><span data-stu-id="07377-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="07377-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07377-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07377-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07377-105">DESCRIPTION</span></span>
<span data-ttu-id="07377-106">Il cmdlet **Get-AzSqlDatabaseGeoBackup** ottiene un backup Geo-ridondante specificato di un database SQL o di tutti i backup Geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="07377-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="07377-107">Un backup Geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica distinta.</span><span class="sxs-lookup"><span data-stu-id="07377-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="07377-108">Puoi usare Geo-Restore per ripristinare un backup Geo-ridondante in caso di interruzioni locali per recuperare il database in una nuova area geografica.</span><span class="sxs-lookup"><span data-stu-id="07377-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="07377-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="07377-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="07377-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07377-110">EXAMPLES</span></span>

### <span data-ttu-id="07377-111">Esempio 1: ottenere tutti i backup Geo-ridondanti in un server</span><span class="sxs-lookup"><span data-stu-id="07377-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="07377-112">Questo comando ottiene tutti i backup Geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="07377-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="07377-113">Esempio 2: ottenere un backup Geo-ridondante specificato</span><span class="sxs-lookup"><span data-stu-id="07377-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="07377-114">Questo comando consente di ottenere il backup Geo-ridondante del database denominato ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="07377-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="07377-115">Esempio 3: ottenere tutti i backup Geo-ridondanti in un server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="07377-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="07377-116">Questo comando ottiene tutti i backup Geo-ridondanti disponibili in un server specificato che inizia con "contoso".</span><span class="sxs-lookup"><span data-stu-id="07377-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="07377-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07377-117">PARAMETERS</span></span>

### <span data-ttu-id="07377-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="07377-118">-DatabaseName</span></span>
<span data-ttu-id="07377-119">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="07377-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="07377-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07377-120">-DefaultProfile</span></span>
<span data-ttu-id="07377-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07377-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07377-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07377-122">-ResourceGroupName</span></span>
<span data-ttu-id="07377-123">Specifica il nome del gruppo di risorse a cui è assegnato il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="07377-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="07377-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="07377-124">-ServerName</span></span>
<span data-ttu-id="07377-125">Specifica il nome del server che ospita il backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="07377-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="07377-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07377-126">-Confirm</span></span>
<span data-ttu-id="07377-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07377-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07377-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07377-128">-WhatIf</span></span>
<span data-ttu-id="07377-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07377-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07377-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07377-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07377-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07377-131">CommonParameters</span></span>
<span data-ttu-id="07377-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07377-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07377-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07377-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07377-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07377-134">INPUTS</span></span>

### <span data-ttu-id="07377-135">System. String</span><span class="sxs-lookup"><span data-stu-id="07377-135">System.String</span></span>

## <span data-ttu-id="07377-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07377-136">OUTPUTS</span></span>

### <span data-ttu-id="07377-137">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="07377-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="07377-138">Note</span><span class="sxs-lookup"><span data-stu-id="07377-138">NOTES</span></span>

## <span data-ttu-id="07377-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07377-139">RELATED LINKS</span></span>

[<span data-ttu-id="07377-140">Panoramica: cloud business continuity e ripristino di emergenza del database con database SQL</span><span class="sxs-lookup"><span data-stu-id="07377-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="07377-141">Recuperare un database SQL di Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="07377-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="07377-142">Ripristinare-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07377-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="07377-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="07377-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
