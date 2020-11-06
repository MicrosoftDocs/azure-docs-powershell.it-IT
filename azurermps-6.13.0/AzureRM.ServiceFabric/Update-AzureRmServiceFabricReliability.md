---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 15dfc29703e2d331920a1751bcd6671e77d84171
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516447"
---
# <span data-ttu-id="fff20-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="fff20-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="fff20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fff20-102">SYNOPSIS</span></span>
<span data-ttu-id="fff20-103">Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.</span><span class="sxs-lookup"><span data-stu-id="fff20-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fff20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fff20-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fff20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fff20-105">DESCRIPTION</span></span>
<span data-ttu-id="fff20-106">Usare **Update-AzureRmServiceFabricReliability** per aggiornare l'affidabilità del tipo di nodo primario in un cluster.</span><span class="sxs-lookup"><span data-stu-id="fff20-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="fff20-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fff20-107">EXAMPLES</span></span>

### <span data-ttu-id="fff20-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fff20-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="fff20-109">Questo comando modifica il livello di affidabilità del tipo di nodo primario in Silver.</span><span class="sxs-lookup"><span data-stu-id="fff20-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="fff20-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fff20-110">PARAMETERS</span></span>

### <span data-ttu-id="fff20-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="fff20-111">-AutoAddNode</span></span>
<span data-ttu-id="fff20-112">Aggiungere automaticamente il conteggio nodi quando si cambia l'affidabilità.</span><span class="sxs-lookup"><span data-stu-id="fff20-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="fff20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff20-113">-DefaultProfile</span></span>
<span data-ttu-id="fff20-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fff20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fff20-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fff20-115">-Name</span></span>
<span data-ttu-id="fff20-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="fff20-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fff20-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="fff20-117">-ReliabilityLevel</span></span>
<span data-ttu-id="fff20-118">Livello di affidabilità.</span><span class="sxs-lookup"><span data-stu-id="fff20-118">Reliability tier.</span></span>

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

### <span data-ttu-id="fff20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff20-119">-ResourceGroupName</span></span>
<span data-ttu-id="fff20-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fff20-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fff20-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fff20-121">-Confirm</span></span>
<span data-ttu-id="fff20-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff20-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff20-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff20-123">-WhatIf</span></span>
<span data-ttu-id="fff20-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fff20-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fff20-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fff20-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff20-126">CommonParameters</span></span>
<span data-ttu-id="fff20-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff20-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fff20-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff20-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fff20-129">INPUTS</span></span>

### <span data-ttu-id="fff20-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fff20-130">System.String</span></span>

### <span data-ttu-id="fff20-131">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="fff20-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="fff20-132">Parametri: ReliabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fff20-132">Parameters: ReliabilityLevel (ByValue)</span></span>

### <span data-ttu-id="fff20-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fff20-133">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="fff20-134">Parametri: AutoAddNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fff20-134">Parameters: AutoAddNode (ByValue)</span></span>

## <span data-ttu-id="fff20-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fff20-135">OUTPUTS</span></span>

### <span data-ttu-id="fff20-136">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fff20-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fff20-137">Note</span><span class="sxs-lookup"><span data-stu-id="fff20-137">NOTES</span></span>

## <span data-ttu-id="fff20-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fff20-138">RELATED LINKS</span></span>
