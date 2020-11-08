---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: 07aa0f8b9d207a460d370e3e5c51b720895b62e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021674"
---
# <span data-ttu-id="9c64b-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="9c64b-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="9c64b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c64b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c64b-103">Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.</span><span class="sxs-lookup"><span data-stu-id="9c64b-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="9c64b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c64b-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c64b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c64b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c64b-106">Usare **Update-AzServiceFabricReliability** per aggiornare l'affidabilità del tipo di nodo primario in un cluster.</span><span class="sxs-lookup"><span data-stu-id="9c64b-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="9c64b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c64b-107">EXAMPLES</span></span>

### <span data-ttu-id="9c64b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c64b-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="9c64b-109">Questo comando modifica il livello di affidabilità del tipo di nodo primario in Silver.</span><span class="sxs-lookup"><span data-stu-id="9c64b-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="9c64b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c64b-110">PARAMETERS</span></span>

### <span data-ttu-id="9c64b-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="9c64b-111">-AutoAddNode</span></span>
<span data-ttu-id="9c64b-112">Aggiungere automaticamente il conteggio nodi quando si cambia l'affidabilità</span><span class="sxs-lookup"><span data-stu-id="9c64b-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c64b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c64b-113">-DefaultProfile</span></span>
<span data-ttu-id="9c64b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c64b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c64b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c64b-115">-Name</span></span>
<span data-ttu-id="9c64b-116">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="9c64b-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c64b-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9c64b-117">-ReliabilityLevel</span></span>
<span data-ttu-id="9c64b-118">Livello di affidabilità</span><span class="sxs-lookup"><span data-stu-id="9c64b-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c64b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c64b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c64b-120">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c64b-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9c64b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c64b-121">-Confirm</span></span>
<span data-ttu-id="9c64b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c64b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c64b-123">-WhatIf</span></span>
<span data-ttu-id="9c64b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c64b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c64b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c64b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c64b-126">CommonParameters</span></span>
<span data-ttu-id="9c64b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c64b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c64b-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c64b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c64b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c64b-129">INPUTS</span></span>

### <span data-ttu-id="9c64b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9c64b-130">System.String</span></span>

### <span data-ttu-id="9c64b-131">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9c64b-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="9c64b-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c64b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c64b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c64b-133">OUTPUTS</span></span>

### <span data-ttu-id="9c64b-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="9c64b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9c64b-135">Note</span><span class="sxs-lookup"><span data-stu-id="9c64b-135">NOTES</span></span>

## <span data-ttu-id="9c64b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c64b-136">RELATED LINKS</span></span>
