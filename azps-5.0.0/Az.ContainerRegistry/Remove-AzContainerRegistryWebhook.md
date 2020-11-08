---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193535"
---
# <span data-ttu-id="e3a05-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="e3a05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3a05-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a05-103">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3a05-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="e3a05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a05-104">SYNTAX</span></span>

### <span data-ttu-id="e3a05-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3a05-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3a05-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3a05-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3a05-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3a05-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a05-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a05-108">DESCRIPTION</span></span>
<span data-ttu-id="e3a05-109">Il cmdlet Remove-AzContainerRegistryWebhook rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3a05-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="e3a05-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a05-110">EXAMPLES</span></span>

### <span data-ttu-id="e3a05-111">Esempio 1: rimuovere un webhook del registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3a05-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="e3a05-112">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3a05-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="e3a05-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3a05-113">PARAMETERS</span></span>

### <span data-ttu-id="e3a05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a05-114">-DefaultProfile</span></span>
<span data-ttu-id="e3a05-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a05-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a05-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3a05-116">-Name</span></span>
<span data-ttu-id="e3a05-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="e3a05-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a05-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3a05-118">-PassThru</span></span>
<span data-ttu-id="e3a05-119">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="e3a05-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="e3a05-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e3a05-120">-RegistryName</span></span>
<span data-ttu-id="e3a05-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3a05-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a05-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a05-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3a05-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3a05-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a05-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a05-124">-ResourceId</span></span>
<span data-ttu-id="e3a05-125">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="e3a05-125">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a05-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-126">-Webhook</span></span>
<span data-ttu-id="e3a05-127">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3a05-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a05-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3a05-128">-Confirm</span></span>
<span data-ttu-id="e3a05-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3a05-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a05-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a05-130">-WhatIf</span></span>
<span data-ttu-id="e3a05-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3a05-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a05-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3a05-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a05-133">CommonParameters</span></span>
<span data-ttu-id="e3a05-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a05-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3a05-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a05-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3a05-136">INPUTS</span></span>

### <span data-ttu-id="e3a05-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="e3a05-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a05-138">System.String</span></span>

## <span data-ttu-id="e3a05-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a05-139">OUTPUTS</span></span>

### <span data-ttu-id="e3a05-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3a05-140">System.Boolean</span></span>

## <span data-ttu-id="e3a05-141">Note</span><span class="sxs-lookup"><span data-stu-id="e3a05-141">NOTES</span></span>

## <span data-ttu-id="e3a05-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a05-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3a05-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e3a05-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e3a05-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e3a05-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3a05-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)