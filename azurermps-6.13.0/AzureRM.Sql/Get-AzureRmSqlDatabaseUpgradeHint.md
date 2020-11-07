---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b289dc637b3d75321120f06eb9ddf604ebcdabba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686891"
---
# <span data-ttu-id="b3e82-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="b3e82-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="b3e82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3e82-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e82-103">Ottiene suggerimenti per i livelli di prezzo per un database.</span><span class="sxs-lookup"><span data-stu-id="b3e82-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3e82-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e82-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e82-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e82-106">Il cmdlet **Get-AzureRmSqlDatabaseUpgradeHint** ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e82-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="b3e82-107">I database ancora in livelli Web e business pricing ottengono il suggerimento per l'aggiornamento ai nuovi livelli di prezzo di base, standard o Premium.</span><span class="sxs-lookup"><span data-stu-id="b3e82-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="b3e82-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e82-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b3e82-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3e82-109">EXAMPLES</span></span>

### <span data-ttu-id="b3e82-110">Esempio 1: ottenere suggerimenti per tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="b3e82-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="b3e82-111">Questo comando restituisce gli hint di aggiornamento per tutti i database sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="b3e82-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="b3e82-112">Esempio 2: ottenere suggerimenti per un database specifico</span><span class="sxs-lookup"><span data-stu-id="b3e82-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b3e82-113">Questo comando restituisce i suggerimenti per l'aggiornamento per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="b3e82-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="b3e82-114">Esempio 3: ottenere suggerimenti per tutti i database che non si trovano in un pool di database elastici</span><span class="sxs-lookup"><span data-stu-id="b3e82-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="b3e82-115">Questo comando restituisce gli hint di aggiornamento per tutti i database che non si trovano in un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="b3e82-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="b3e82-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3e82-116">PARAMETERS</span></span>

### <span data-ttu-id="b3e82-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3e82-117">-DatabaseName</span></span>
<span data-ttu-id="b3e82-118">Specifica il nome del database SQL per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b3e82-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="b3e82-119">Se non si specifica un database, questo cmdlet ottiene i suggerimenti per tutti i database nel server logico.</span><span class="sxs-lookup"><span data-stu-id="b3e82-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="b3e82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e82-120">-DefaultProfile</span></span>
<span data-ttu-id="b3e82-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3e82-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3e82-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="b3e82-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="b3e82-123">Indica se i database in pool di database elastici sono esclusi dai suggerimenti restituiti.</span><span class="sxs-lookup"><span data-stu-id="b3e82-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="b3e82-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e82-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3e82-125">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="b3e82-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b3e82-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b3e82-126">-ServerName</span></span>
<span data-ttu-id="b3e82-127">Specifica il nome del server che ospita il database per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b3e82-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="b3e82-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3e82-128">-Confirm</span></span>
<span data-ttu-id="b3e82-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3e82-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e82-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e82-130">-WhatIf</span></span>
<span data-ttu-id="b3e82-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3e82-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e82-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3e82-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e82-133">CommonParameters</span></span>
<span data-ttu-id="b3e82-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e82-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e82-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e82-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3e82-136">INPUTS</span></span>

### <span data-ttu-id="b3e82-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e82-137">System.String</span></span>

### <span data-ttu-id="b3e82-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3e82-138">System.Boolean</span></span>

## <span data-ttu-id="b3e82-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3e82-139">OUTPUTS</span></span>

### <span data-ttu-id="b3e82-140">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="b3e82-140">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="b3e82-141">Note</span><span class="sxs-lookup"><span data-stu-id="b3e82-141">NOTES</span></span>

## <span data-ttu-id="b3e82-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3e82-142">RELATED LINKS</span></span>

[<span data-ttu-id="b3e82-143">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b3e82-143">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="b3e82-144">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="b3e82-144">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


