---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: ad46883722f0c9d4c4d8bf5a5f5f568bb267bba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688226"
---
# <span data-ttu-id="37e5a-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="37e5a-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="37e5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="37e5a-103">Ottiene un backup Geo-ridondante di un database.</span><span class="sxs-lookup"><span data-stu-id="37e5a-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37e5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37e5a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e5a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="37e5a-106">Il cmdlet **Get-AzureRMSqlDatabaseGeoBackup** ottiene un backup Geo-ridondante specificato di un database SQL o di tutti i backup Geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="37e5a-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="37e5a-107">Un backup Geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica distinta.</span><span class="sxs-lookup"><span data-stu-id="37e5a-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="37e5a-108">Puoi usare Geo-Restore per ripristinare un backup Geo-ridondante in caso di interruzioni locali per recuperare il database in una nuova area geografica.</span><span class="sxs-lookup"><span data-stu-id="37e5a-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="37e5a-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="37e5a-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="37e5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37e5a-110">EXAMPLES</span></span>

### <span data-ttu-id="37e5a-111">Esempio 1: ottenere tutti i backup Geo-ridondanti in un server</span><span class="sxs-lookup"><span data-stu-id="37e5a-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="37e5a-112">Questo comando ottiene tutti i backup Geo-ridondanti disponibili in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="37e5a-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="37e5a-113">Esempio 2: ottenere un backup Geo-ridondante specificato</span><span class="sxs-lookup"><span data-stu-id="37e5a-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="37e5a-114">Questo comando consente di ottenere il backup Geo-ridondante del database denominato ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="37e5a-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="37e5a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37e5a-115">PARAMETERS</span></span>

### <span data-ttu-id="37e5a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37e5a-116">-DatabaseName</span></span>
<span data-ttu-id="37e5a-117">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="37e5a-117">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="37e5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e5a-118">-ResourceGroupName</span></span>
<span data-ttu-id="37e5a-119">Specifica il nome del gruppo di risorse a cui è assegnato il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="37e5a-119">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="37e5a-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="37e5a-120">-ServerName</span></span>
<span data-ttu-id="37e5a-121">Specifica il nome del server che ospita il backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="37e5a-121">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="37e5a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37e5a-122">-Confirm</span></span>
<span data-ttu-id="37e5a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e5a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e5a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e5a-124">-WhatIf</span></span>
<span data-ttu-id="37e5a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37e5a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e5a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37e5a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e5a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e5a-127">-DefaultProfile</span></span>
<span data-ttu-id="37e5a-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37e5a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e5a-129">CommonParameters</span></span>
<span data-ttu-id="37e5a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e5a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e5a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e5a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37e5a-132">INPUTS</span></span>

## <span data-ttu-id="37e5a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37e5a-133">OUTPUTS</span></span>

### <span data-ttu-id="37e5a-134">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="37e5a-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="37e5a-135">Note</span><span class="sxs-lookup"><span data-stu-id="37e5a-135">NOTES</span></span>

## <span data-ttu-id="37e5a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37e5a-136">RELATED LINKS</span></span>

[<span data-ttu-id="37e5a-137">Panoramica: cloud business continuity e ripristino di emergenza del database con database SQL</span><span class="sxs-lookup"><span data-stu-id="37e5a-137">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="37e5a-138">Recuperare un database SQL di Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="37e5a-138">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="37e5a-139">Ripristinare-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37e5a-139">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="37e5a-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="37e5a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
