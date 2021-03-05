---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014670"
---
# <span data-ttu-id="e6ac5-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="e6ac5-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="e6ac5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ac5-103">Ottiene suggerimenti sui prezzi per un database.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="e6ac5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6ac5-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ac5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ac5-106">Il cmdlet **Get-AzSqlDatabaseUpgradeHint** ottiene suggerimenti per i prezzi per l'aggiornamento di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="e6ac5-107">I database ancora in livelli di prezzi Web e Business ottengono l'suggerimento di passare ai nuovi livelli di prezzi Basic, Standard o Premium.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="e6ac5-108">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e6ac5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6ac5-109">EXAMPLES</span></span>

### <span data-ttu-id="e6ac5-110">Esempio 1: Suggerimenti per tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="e6ac5-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e6ac5-111">Questo comando restituisce suggerimenti per l'aggiornamento per tutti i database sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="e6ac5-112">Esempio 2: Suggerimenti per un database specifico</span><span class="sxs-lookup"><span data-stu-id="e6ac5-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e6ac5-113">Questo comando restituisce suggerimenti per l'aggiornamento per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="e6ac5-114">Esempio 3: Ottenere suggerimenti per tutti i database non presenti in un pool di database flessibile</span><span class="sxs-lookup"><span data-stu-id="e6ac5-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="e6ac5-115">Questo comando restituisce suggerimenti per l'aggiornamento per tutti i database non presenti in un pool di database flessibile.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="e6ac5-116">Esempio 4: Ottenere suggerimenti per tutti i database in un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="e6ac5-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="e6ac5-117">Questo comando restituisce suggerimenti per l'aggiornamento per tutti i database nel server denominato Server01 che iniziano con "Database".</span><span class="sxs-lookup"><span data-stu-id="e6ac5-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="e6ac5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ac5-118">PARAMETERS</span></span>

### <span data-ttu-id="e6ac5-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6ac5-119">-DatabaseName</span></span>
<span data-ttu-id="e6ac5-120">Specifica il nome del database di SQL per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="e6ac5-121">Se non si specifica un database, questo cmdlet ottiene suggerimenti per tutti i database nel server logico.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ac5-122">-DefaultProfile</span></span>
<span data-ttu-id="e6ac5-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e6ac5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6ac5-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="e6ac5-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="e6ac5-125">Indica se i database in pool di database elastici sono esclusi dai suggerimenti restituiti.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ac5-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6ac5-127">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e6ac5-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6ac5-128">-ServerName</span></span>
<span data-ttu-id="e6ac5-129">Specifica il nome del server che ospita il database per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="e6ac5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6ac5-130">-Confirm</span></span>
<span data-ttu-id="e6ac5-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ac5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ac5-132">-WhatIf</span></span>
<span data-ttu-id="e6ac5-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ac5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ac5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ac5-135">CommonParameters</span></span>
<span data-ttu-id="e6ac5-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ac5-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6ac5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ac5-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6ac5-138">INPUTS</span></span>

### <span data-ttu-id="e6ac5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e6ac5-139">System.String</span></span>

### <span data-ttu-id="e6ac5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6ac5-140">System.Boolean</span></span>

## <span data-ttu-id="e6ac5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6ac5-141">OUTPUTS</span></span>

### <span data-ttu-id="e6ac5-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="e6ac5-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="e6ac5-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6ac5-143">NOTES</span></span>

## <span data-ttu-id="e6ac5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6ac5-144">RELATED LINKS</span></span>

[<span data-ttu-id="e6ac5-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="e6ac5-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="e6ac5-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="e6ac5-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


