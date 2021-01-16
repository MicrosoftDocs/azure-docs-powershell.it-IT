---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355096"
---
# <span data-ttu-id="aa7fb-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="aa7fb-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="aa7fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7fb-103">Ottiene suggerimenti per i pool elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="aa7fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa7fb-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa7fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa7fb-105">DESCRIPTION</span></span>
<span data-ttu-id="aa7fb-106">Il cmdlet **Get-AzSqlElasticPoolRecommendation** ottiene suggerimenti per i pool elastici per un server.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="aa7fb-107">Questi suggerimenti includono i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa7fb-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="aa7fb-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-108">DatabaseCollection.</span></span> <span data-ttu-id="aa7fb-109">Raccolta di nomi di database che appartengono al pool.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="aa7fb-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-110">DatabaseDtuMin.</span></span> <span data-ttu-id="aa7fb-111">Unità di trasmissione dati (DTU) garanzia per i database nel pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="aa7fb-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="aa7fb-113">DTU Cap per i database nel pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="aa7fb-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-114">Dtu.</span></span> <span data-ttu-id="aa7fb-115">Garanzia DTU per il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="aa7fb-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-116">StorageMb.</span></span> <span data-ttu-id="aa7fb-117">Archiviazione in megabyte per il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="aa7fb-118">Edizione.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-118">Edition.</span></span> <span data-ttu-id="aa7fb-119">Edition per il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-119">Edition for the elastic pool.</span></span> <span data-ttu-id="aa7fb-120">I valori accettabili per questo parametro sono: Basic, standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="aa7fb-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-121">IncludeAllDatabases.</span></span> <span data-ttu-id="aa7fb-122">Indica se vengono restituiti tutti i database nel pool elastico.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="aa7fb-123">Nome.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-123">Name.</span></span> <span data-ttu-id="aa7fb-124">Nome del pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="aa7fb-125">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa7fb-125">EXAMPLES</span></span>

### <span data-ttu-id="aa7fb-126">Esempio 1: ottenere suggerimenti per un server</span><span class="sxs-lookup"><span data-stu-id="aa7fb-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="aa7fb-127">Questo comando ottiene i consigli per il pool elastici per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="aa7fb-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa7fb-128">PARAMETERS</span></span>

### <span data-ttu-id="aa7fb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7fb-129">-DefaultProfile</span></span>
<span data-ttu-id="aa7fb-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aa7fb-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa7fb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7fb-131">-ResourceGroupName</span></span>
<span data-ttu-id="aa7fb-132">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="aa7fb-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="aa7fb-133">-ServerName</span></span>
<span data-ttu-id="aa7fb-134">Specifica il nome del server per cui questo cmdlet ottiene i suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="aa7fb-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa7fb-135">-Confirm</span></span>
<span data-ttu-id="aa7fb-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa7fb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa7fb-137">-WhatIf</span></span>
<span data-ttu-id="aa7fb-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa7fb-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa7fb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7fb-140">CommonParameters</span></span>
<span data-ttu-id="aa7fb-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7fb-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa7fb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7fb-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa7fb-143">INPUTS</span></span>

### <span data-ttu-id="aa7fb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aa7fb-144">System.String</span></span>

## <span data-ttu-id="aa7fb-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa7fb-145">OUTPUTS</span></span>

### <span data-ttu-id="aa7fb-146">Microsoft. Azure. Management. SQL. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="aa7fb-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="aa7fb-147">Note</span><span class="sxs-lookup"><span data-stu-id="aa7fb-147">NOTES</span></span>

## <span data-ttu-id="aa7fb-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa7fb-148">RELATED LINKS</span></span>
