---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188095"
---
# <span data-ttu-id="14e9e-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="14e9e-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="14e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="14e9e-103">Ottiene suggerimenti sul pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="14e9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14e9e-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14e9e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="14e9e-106">Il cmdlet **Get-AzSqlElasticPoolRecommendation** ottiene suggerimenti per il pool flessibile per un server.</span><span class="sxs-lookup"><span data-stu-id="14e9e-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="14e9e-107">Questi suggerimenti includono i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="14e9e-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="14e9e-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="14e9e-108">DatabaseCollection.</span></span> <span data-ttu-id="14e9e-109">Raccolta di nomi di database che appartengono al pool.</span><span class="sxs-lookup"><span data-stu-id="14e9e-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="14e9e-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="14e9e-110">DatabaseDtuMin.</span></span> <span data-ttu-id="14e9e-111">Garanzia dell'unità di trasmissione dati per i database nel pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="14e9e-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="14e9e-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="14e9e-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="14e9e-113">Limite DTU per i database nel pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="14e9e-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="14e9e-114">Dtu.</span></span> <span data-ttu-id="14e9e-115">Garanzia DTU per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="14e9e-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="14e9e-116">StorageMb.</span></span> <span data-ttu-id="14e9e-117">Spazio di archiviazione in megabyte per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="14e9e-118">Edizione.</span><span class="sxs-lookup"><span data-stu-id="14e9e-118">Edition.</span></span> <span data-ttu-id="14e9e-119">Edizione per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-119">Edition for the elastic pool.</span></span> <span data-ttu-id="14e9e-120">I valori accettabili per questo parametro sono: Basic, Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="14e9e-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="14e9e-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="14e9e-121">IncludeAllDatabases.</span></span> <span data-ttu-id="14e9e-122">Indica se vengono restituiti tutti i database nel pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="14e9e-123">Nome.</span><span class="sxs-lookup"><span data-stu-id="14e9e-123">Name.</span></span> <span data-ttu-id="14e9e-124">Nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="14e9e-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="14e9e-125">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14e9e-125">EXAMPLES</span></span>

### <span data-ttu-id="14e9e-126">Esempio 1: Ottenere suggerimenti per un server</span><span class="sxs-lookup"><span data-stu-id="14e9e-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="14e9e-127">Questo comando recupera i suggerimenti per il pool flessibile per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="14e9e-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="14e9e-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e9e-128">PARAMETERS</span></span>

### <span data-ttu-id="14e9e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e9e-129">-DefaultProfile</span></span>
<span data-ttu-id="14e9e-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="14e9e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14e9e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e9e-131">-ResourceGroupName</span></span>
<span data-ttu-id="14e9e-132">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="14e9e-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="14e9e-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="14e9e-133">-ServerName</span></span>
<span data-ttu-id="14e9e-134">Specifica il nome del server per cui il cmdlet riceve consigli.</span><span class="sxs-lookup"><span data-stu-id="14e9e-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="14e9e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e9e-135">-Confirm</span></span>
<span data-ttu-id="14e9e-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14e9e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e9e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e9e-137">-WhatIf</span></span>
<span data-ttu-id="14e9e-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14e9e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e9e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14e9e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e9e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e9e-140">CommonParameters</span></span>
<span data-ttu-id="14e9e-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e9e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e9e-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14e9e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e9e-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="14e9e-143">INPUTS</span></span>

### <span data-ttu-id="14e9e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="14e9e-144">System.String</span></span>

## <span data-ttu-id="14e9e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14e9e-145">OUTPUTS</span></span>

### <span data-ttu-id="14e9e-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="14e9e-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="14e9e-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="14e9e-147">NOTES</span></span>

## <span data-ttu-id="14e9e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14e9e-148">RELATED LINKS</span></span>
