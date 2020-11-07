---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: 79e4919278e034c97b224c17538edfebfbf51a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686676"
---
# <span data-ttu-id="103e3-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="103e3-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="103e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="103e3-102">SYNOPSIS</span></span>
<span data-ttu-id="103e3-103">Ottiene un backup Geo-ridondante di un database.</span><span class="sxs-lookup"><span data-stu-id="103e3-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="103e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="103e3-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="103e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="103e3-105">DESCRIPTION</span></span>
<span data-ttu-id="103e3-106">Il cmdlet **Get-AzureRMSqlDatabaseGeoBackup** ottiene un backup Geo-ridondante specificato di un database SQL o di tutti i backup Geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="103e3-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="103e3-107">Un backup Geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica distinta.</span><span class="sxs-lookup"><span data-stu-id="103e3-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="103e3-108">Puoi usare Geo-Restore per ripristinare un backup Geo-ridondante in caso di interruzioni locali per recuperare il database in una nuova area geografica.</span><span class="sxs-lookup"><span data-stu-id="103e3-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="103e3-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="103e3-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="103e3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="103e3-110">EXAMPLES</span></span>

### <span data-ttu-id="103e3-111">Esempio 1: ottenere tutti i backup Geo-ridondanti in un server</span><span class="sxs-lookup"><span data-stu-id="103e3-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="103e3-112">Questo comando ottiene tutti i backup Geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="103e3-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="103e3-113">Esempio 2: ottenere un backup Geo-ridondante specificato</span><span class="sxs-lookup"><span data-stu-id="103e3-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="103e3-114">Questo comando consente di ottenere il backup Geo-ridondante del database denominato ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="103e3-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="103e3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="103e3-115">PARAMETERS</span></span>

### <span data-ttu-id="103e3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="103e3-116">-DatabaseName</span></span>
<span data-ttu-id="103e3-117">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="103e3-117">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103e3-118">-DefaultProfile</span></span>
<span data-ttu-id="103e3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="103e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="103e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="103e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="103e3-121">Specifica il nome del gruppo di risorse a cui è assegnato il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="103e3-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103e3-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="103e3-122">-ServerName</span></span>
<span data-ttu-id="103e3-123">Specifica il nome del server che ospita il backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="103e3-123">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103e3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="103e3-124">-Confirm</span></span>
<span data-ttu-id="103e3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="103e3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="103e3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103e3-126">-WhatIf</span></span>
<span data-ttu-id="103e3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="103e3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="103e3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="103e3-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="103e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103e3-129">CommonParameters</span></span>
<span data-ttu-id="103e3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103e3-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="103e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103e3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="103e3-132">INPUTS</span></span>

### <span data-ttu-id="103e3-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="103e3-133">None</span></span>
<span data-ttu-id="103e3-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="103e3-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="103e3-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="103e3-135">OUTPUTS</span></span>

### <span data-ttu-id="103e3-136">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="103e3-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="103e3-137">Note</span><span class="sxs-lookup"><span data-stu-id="103e3-137">NOTES</span></span>

## <span data-ttu-id="103e3-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="103e3-138">RELATED LINKS</span></span>

[<span data-ttu-id="103e3-139">Panoramica: cloud business continuity e ripristino di emergenza del database con database SQL</span><span class="sxs-lookup"><span data-stu-id="103e3-139">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="103e3-140">Recuperare un database SQL di Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="103e3-140">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="103e3-141">Ripristinare-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="103e3-141">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="103e3-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="103e3-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
