---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189482"
---
# <span data-ttu-id="b2821-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="b2821-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="b2821-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2821-102">SYNOPSIS</span></span>
<span data-ttu-id="b2821-103">Reimposta la RoutingState di una risorsa VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b2821-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="b2821-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2821-104">SYNTAX</span></span>

### <span data-ttu-id="b2821-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2821-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2821-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b2821-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2821-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b2821-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2821-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2821-108">DESCRIPTION</span></span>
<span data-ttu-id="b2821-109">Reimposta lo stato di routing di una risorsa VirtualHub esistente solo se non viene effettuato il provisioning dello stato di routing dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2821-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="b2821-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2821-110">EXAMPLES</span></span>

### <span data-ttu-id="b2821-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2821-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="b2821-112">Reimposta lo stato di routing dell'hub virtuale usando il relativo ResourceGroupName e il resourceName.</span><span class="sxs-lookup"><span data-stu-id="b2821-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="b2821-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b2821-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="b2821-114">Reimposta lo stato di routing dell'hub virtuale usando il relativo ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b2821-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="b2821-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b2821-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="b2821-116">Reimposta lo stato di routing dell'hub virtuale usando un oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="b2821-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="b2821-117">L'oggetto di input è di tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b2821-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="b2821-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b2821-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="b2821-119">Un oggetto hub virtuale esistente può essere recuperato e quindi passato come oggetto di input a Reset-AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="b2821-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="b2821-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2821-120">PARAMETERS</span></span>

### <span data-ttu-id="b2821-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2821-121">-AsJob</span></span>
<span data-ttu-id="b2821-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b2821-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2821-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2821-123">-DefaultProfile</span></span>
<span data-ttu-id="b2821-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2821-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2821-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b2821-125">-Force</span></span>
<span data-ttu-id="b2821-126">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="b2821-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2821-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2821-127">-InputObject</span></span>
<span data-ttu-id="b2821-128">L'oggetto hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="b2821-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2821-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2821-129">-Name</span></span>
<span data-ttu-id="b2821-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2821-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2821-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2821-131">-ResourceGroupName</span></span>
<span data-ttu-id="b2821-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2821-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2821-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2821-133">-ResourceId</span></span>
<span data-ttu-id="b2821-134">ID risorsa dell'hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="b2821-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2821-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2821-135">-Confirm</span></span>
<span data-ttu-id="b2821-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2821-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2821-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2821-137">-WhatIf</span></span>
<span data-ttu-id="b2821-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2821-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2821-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2821-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2821-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2821-140">CommonParameters</span></span>
<span data-ttu-id="b2821-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2821-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2821-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2821-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2821-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2821-143">INPUTS</span></span>

### <span data-ttu-id="b2821-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b2821-144">System.String</span></span>

### <span data-ttu-id="b2821-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b2821-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b2821-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2821-146">OUTPUTS</span></span>

### <span data-ttu-id="b2821-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b2821-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b2821-148">Note</span><span class="sxs-lookup"><span data-stu-id="b2821-148">NOTES</span></span>

## <span data-ttu-id="b2821-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2821-149">RELATED LINKS</span></span>

[<span data-ttu-id="b2821-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b2821-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
