---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 47d56a0c15cc3ecf9656ae6c14600adf6a1e2cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512835"
---
# <span data-ttu-id="fe50e-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="fe50e-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="fe50e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe50e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe50e-103">Ottiene suggerimenti per i pool elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe50e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe50e-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe50e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe50e-105">DESCRIPTION</span></span>
<span data-ttu-id="fe50e-106">Il cmdlet **Get-AzureRmSqlElasticPoolRecommendation** ottiene suggerimenti per i pool elastici per un server.</span><span class="sxs-lookup"><span data-stu-id="fe50e-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="fe50e-107">Questi suggerimenti includono i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe50e-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="fe50e-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="fe50e-108">DatabaseCollection.</span></span> <span data-ttu-id="fe50e-109">Raccolta di nomi di database che appartengono al pool.</span><span class="sxs-lookup"><span data-stu-id="fe50e-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="fe50e-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="fe50e-110">DatabaseDtuMin.</span></span> <span data-ttu-id="fe50e-111">Unità di trasmissione dati (DTU) garanzia per i database nel pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="fe50e-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="fe50e-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="fe50e-113">DTU Cap per i database nel pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="fe50e-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="fe50e-114">Dtu.</span></span> <span data-ttu-id="fe50e-115">Garanzia DTU per il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="fe50e-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="fe50e-116">StorageMb.</span></span> <span data-ttu-id="fe50e-117">Archiviazione in megabyte per il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="fe50e-118">Edizione.</span><span class="sxs-lookup"><span data-stu-id="fe50e-118">Edition.</span></span> <span data-ttu-id="fe50e-119">Edition per il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-119">Edition for the elastic pool.</span></span> <span data-ttu-id="fe50e-120">I valori accettabili per questo parametro sono: Basic, standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="fe50e-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="fe50e-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="fe50e-121">IncludeAllDatabases.</span></span> <span data-ttu-id="fe50e-122">Indica se vengono restituiti tutti i database nel pool elastico.</span><span class="sxs-lookup"><span data-stu-id="fe50e-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="fe50e-123">Nome.</span><span class="sxs-lookup"><span data-stu-id="fe50e-123">Name.</span></span> <span data-ttu-id="fe50e-124">Nome del pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="fe50e-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="fe50e-125">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe50e-125">EXAMPLES</span></span>

### <span data-ttu-id="fe50e-126">Esempio 1: ottenere suggerimenti per un server</span><span class="sxs-lookup"><span data-stu-id="fe50e-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="fe50e-127">Questo comando ottiene i consigli per il pool elastici per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="fe50e-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="fe50e-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe50e-128">PARAMETERS</span></span>

### <span data-ttu-id="fe50e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe50e-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe50e-130">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="fe50e-130">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fe50e-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fe50e-131">-ServerName</span></span>
<span data-ttu-id="fe50e-132">Specifica il nome del server per cui questo cmdlet ottiene i suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="fe50e-132">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="fe50e-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe50e-133">-Confirm</span></span>
<span data-ttu-id="fe50e-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe50e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe50e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe50e-135">-WhatIf</span></span>
<span data-ttu-id="fe50e-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe50e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe50e-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe50e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe50e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe50e-138">-DefaultProfile</span></span>
<span data-ttu-id="fe50e-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe50e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe50e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe50e-140">CommonParameters</span></span>
<span data-ttu-id="fe50e-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe50e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe50e-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe50e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe50e-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe50e-143">INPUTS</span></span>

## <span data-ttu-id="fe50e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe50e-144">OUTPUTS</span></span>

## <span data-ttu-id="fe50e-145">Note</span><span class="sxs-lookup"><span data-stu-id="fe50e-145">NOTES</span></span>

## <span data-ttu-id="fe50e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe50e-146">RELATED LINKS</span></span>

