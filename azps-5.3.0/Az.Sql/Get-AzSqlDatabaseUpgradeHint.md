---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473689"
---
# <span data-ttu-id="2f832-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="2f832-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="2f832-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f832-102">SYNOPSIS</span></span>
<span data-ttu-id="2f832-103">Ottiene suggerimenti per i livelli di prezzo per un database.</span><span class="sxs-lookup"><span data-stu-id="2f832-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="2f832-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f832-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f832-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f832-105">DESCRIPTION</span></span>
<span data-ttu-id="2f832-106">Il cmdlet **Get-AzSqlDatabaseUpgradeHint** ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2f832-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="2f832-107">I database ancora in livelli Web e business pricing ottengono il suggerimento per l'aggiornamento ai nuovi livelli di prezzo di base, standard o Premium.</span><span class="sxs-lookup"><span data-stu-id="2f832-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="2f832-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="2f832-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2f832-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f832-109">EXAMPLES</span></span>

### <span data-ttu-id="2f832-110">Esempio 1: ottenere suggerimenti per tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="2f832-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="2f832-111">Questo comando restituisce gli hint di aggiornamento per tutti i database sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="2f832-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="2f832-112">Esempio 2: ottenere suggerimenti per un database specifico</span><span class="sxs-lookup"><span data-stu-id="2f832-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="2f832-113">Questo comando restituisce i suggerimenti per l'aggiornamento per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="2f832-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="2f832-114">Esempio 3: ottenere suggerimenti per tutti i database che non si trovano in un pool di database elastici</span><span class="sxs-lookup"><span data-stu-id="2f832-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="2f832-115">Questo comando restituisce gli hint di aggiornamento per tutti i database che non si trovano in un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="2f832-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="2f832-116">Esempio 4: ottenere suggerimenti per tutti i database in un server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="2f832-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="2f832-117">Questo comando restituisce gli hint di aggiornamento per tutti i database sul server denominato Server01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="2f832-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="2f832-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f832-118">PARAMETERS</span></span>

### <span data-ttu-id="2f832-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f832-119">-DatabaseName</span></span>
<span data-ttu-id="2f832-120">Specifica il nome del database SQL per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2f832-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="2f832-121">Se non si specifica un database, questo cmdlet ottiene i suggerimenti per tutti i database nel server logico.</span><span class="sxs-lookup"><span data-stu-id="2f832-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="2f832-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f832-122">-DefaultProfile</span></span>
<span data-ttu-id="2f832-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2f832-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f832-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="2f832-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="2f832-125">Indica se i database in pool di database elastici sono esclusi dai suggerimenti restituiti.</span><span class="sxs-lookup"><span data-stu-id="2f832-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="2f832-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f832-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f832-127">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="2f832-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2f832-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2f832-128">-ServerName</span></span>
<span data-ttu-id="2f832-129">Specifica il nome del server che ospita il database per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2f832-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="2f832-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2f832-130">-Confirm</span></span>
<span data-ttu-id="2f832-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f832-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f832-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f832-132">-WhatIf</span></span>
<span data-ttu-id="2f832-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f832-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f832-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f832-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f832-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f832-135">CommonParameters</span></span>
<span data-ttu-id="2f832-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f832-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f832-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f832-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f832-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f832-138">INPUTS</span></span>

### <span data-ttu-id="2f832-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2f832-139">System.String</span></span>

### <span data-ttu-id="2f832-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f832-140">System.Boolean</span></span>

## <span data-ttu-id="2f832-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f832-141">OUTPUTS</span></span>

### <span data-ttu-id="2f832-142">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="2f832-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="2f832-143">Note</span><span class="sxs-lookup"><span data-stu-id="2f832-143">NOTES</span></span>

## <span data-ttu-id="2f832-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f832-144">RELATED LINKS</span></span>

[<span data-ttu-id="2f832-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="2f832-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="2f832-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="2f832-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


