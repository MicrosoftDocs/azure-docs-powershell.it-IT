---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178510"
---
# <span data-ttu-id="2bcf8-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="2bcf8-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="2bcf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bcf8-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcf8-103">Ottiene suggerimenti sui prezzi per un database.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="2bcf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bcf8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bcf8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2bcf8-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcf8-106">Il cmdlet **Get-AzSqlDatabaseUpgradeHint** ottiene suggerimenti per i prezzi per l'aggiornamento di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="2bcf8-107">I database ancora in livelli di prezzi Web e Business ottengono l'suggerimento di passare ai nuovi livelli di prezzi Basic, Standard o Premium.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="2bcf8-108">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2bcf8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bcf8-109">EXAMPLES</span></span>

### <span data-ttu-id="2bcf8-110">Esempio 1: Suggerimenti per tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="2bcf8-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="2bcf8-111">Questo comando restituisce suggerimenti per l'aggiornamento per tutti i database sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="2bcf8-112">Esempio 2: Suggerimenti per un database specifico</span><span class="sxs-lookup"><span data-stu-id="2bcf8-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="2bcf8-113">Questo comando restituisce suggerimenti per l'aggiornamento per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="2bcf8-114">Esempio 3: Ottenere suggerimenti per tutti i database non presenti in un pool di database flessibile</span><span class="sxs-lookup"><span data-stu-id="2bcf8-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="2bcf8-115">Questo comando restituisce suggerimenti per l'aggiornamento per tutti i database non presenti in un pool di database flessibile.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="2bcf8-116">Esempio 4: Ottenere suggerimenti per tutti i database in un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="2bcf8-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="2bcf8-117">Questo comando restituisce suggerimenti per l'aggiornamento per tutti i database nel server denominato Server01 che iniziano con "Database".</span><span class="sxs-lookup"><span data-stu-id="2bcf8-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="2bcf8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bcf8-118">PARAMETERS</span></span>

### <span data-ttu-id="2bcf8-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2bcf8-119">-DatabaseName</span></span>
<span data-ttu-id="2bcf8-120">Specifica il nome del database di SQL per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="2bcf8-121">Se non si specifica un database, questo cmdlet ottiene suggerimenti per tutti i database nel server logico.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="2bcf8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcf8-122">-DefaultProfile</span></span>
<span data-ttu-id="2bcf8-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2bcf8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bcf8-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="2bcf8-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="2bcf8-125">Indica se i database in pool di database elastici sono esclusi dai suggerimenti restituiti.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="2bcf8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bcf8-126">-ResourceGroupName</span></span>
<span data-ttu-id="2bcf8-127">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2bcf8-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2bcf8-128">-ServerName</span></span>
<span data-ttu-id="2bcf8-129">Specifica il nome del server che ospita il database per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="2bcf8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bcf8-130">-Confirm</span></span>
<span data-ttu-id="2bcf8-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bcf8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bcf8-132">-WhatIf</span></span>
<span data-ttu-id="2bcf8-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bcf8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bcf8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcf8-135">CommonParameters</span></span>
<span data-ttu-id="2bcf8-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcf8-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2bcf8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcf8-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="2bcf8-138">INPUTS</span></span>

### <span data-ttu-id="2bcf8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2bcf8-139">System.String</span></span>

### <span data-ttu-id="2bcf8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2bcf8-140">System.Boolean</span></span>

## <span data-ttu-id="2bcf8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bcf8-141">OUTPUTS</span></span>

### <span data-ttu-id="2bcf8-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="2bcf8-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="2bcf8-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="2bcf8-143">NOTES</span></span>

## <span data-ttu-id="2bcf8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bcf8-144">RELATED LINKS</span></span>

[<span data-ttu-id="2bcf8-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="2bcf8-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="2bcf8-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="2bcf8-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


