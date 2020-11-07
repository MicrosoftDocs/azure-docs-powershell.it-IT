---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676960"
---
# <span data-ttu-id="6f598-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="6f598-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="6f598-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f598-102">SYNOPSIS</span></span>
<span data-ttu-id="6f598-103">Ottiene suggerimenti per i livelli di prezzo per un database.</span><span class="sxs-lookup"><span data-stu-id="6f598-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="6f598-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f598-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f598-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f598-105">DESCRIPTION</span></span>
<span data-ttu-id="6f598-106">Il cmdlet **Get-AzSqlDatabaseUpgradeHint** ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f598-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="6f598-107">I database ancora in livelli Web e business pricing ottengono il suggerimento per l'aggiornamento ai nuovi livelli di prezzo di base, standard o Premium.</span><span class="sxs-lookup"><span data-stu-id="6f598-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="6f598-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="6f598-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6f598-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f598-109">EXAMPLES</span></span>

### <span data-ttu-id="6f598-110">Esempio 1: ottenere suggerimenti per tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="6f598-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="6f598-111">Questo comando restituisce gli hint di aggiornamento per tutti i database sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="6f598-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="6f598-112">Esempio 2: ottenere suggerimenti per un database specifico</span><span class="sxs-lookup"><span data-stu-id="6f598-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6f598-113">Questo comando restituisce i suggerimenti per l'aggiornamento per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="6f598-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="6f598-114">Esempio 3: ottenere suggerimenti per tutti i database che non si trovano in un pool di database elastici</span><span class="sxs-lookup"><span data-stu-id="6f598-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="6f598-115">Questo comando restituisce gli hint di aggiornamento per tutti i database che non si trovano in un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="6f598-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="6f598-116">Esempio 4: ottenere suggerimenti per tutti i database in un server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="6f598-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="6f598-117">Questo comando restituisce gli hint di aggiornamento per tutti i database sul server denominato Server01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="6f598-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="6f598-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f598-118">PARAMETERS</span></span>

### <span data-ttu-id="6f598-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f598-119">-DatabaseName</span></span>
<span data-ttu-id="6f598-120">Specifica il nome del database SQL per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6f598-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="6f598-121">Se non si specifica un database, questo cmdlet ottiene i suggerimenti per tutti i database nel server logico.</span><span class="sxs-lookup"><span data-stu-id="6f598-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6f598-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f598-122">-DefaultProfile</span></span>
<span data-ttu-id="6f598-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6f598-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f598-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="6f598-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="6f598-125">Indica se i database in pool di database elastici sono esclusi dai suggerimenti restituiti.</span><span class="sxs-lookup"><span data-stu-id="6f598-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="6f598-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f598-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f598-127">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="6f598-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6f598-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6f598-128">-ServerName</span></span>
<span data-ttu-id="6f598-129">Specifica il nome del server che ospita il database per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6f598-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="6f598-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6f598-130">-Confirm</span></span>
<span data-ttu-id="6f598-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f598-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f598-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f598-132">-WhatIf</span></span>
<span data-ttu-id="6f598-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f598-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f598-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f598-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f598-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f598-135">CommonParameters</span></span>
<span data-ttu-id="6f598-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f598-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f598-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f598-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f598-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f598-138">INPUTS</span></span>

### <span data-ttu-id="6f598-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6f598-139">System.String</span></span>

### <span data-ttu-id="6f598-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f598-140">System.Boolean</span></span>

## <span data-ttu-id="6f598-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f598-141">OUTPUTS</span></span>

### <span data-ttu-id="6f598-142">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="6f598-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="6f598-143">Note</span><span class="sxs-lookup"><span data-stu-id="6f598-143">NOTES</span></span>

## <span data-ttu-id="6f598-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f598-144">RELATED LINKS</span></span>

[<span data-ttu-id="6f598-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6f598-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="6f598-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f598-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

