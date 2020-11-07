---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1c96b33fd93082c33dfb49abdf23fac8795b2b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684639"
---
# <span data-ttu-id="ff7f1-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="ff7f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7f1-103">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="ff7f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff7f1-104">SYNTAX</span></span>

### <span data-ttu-id="ff7f1-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff7f1-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7f1-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff7f1-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7f1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff7f1-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff7f1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff7f1-108">DESCRIPTION</span></span>
<span data-ttu-id="ff7f1-109">Il cmdlet Remove-AzContainerRegistryWebhook rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="ff7f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff7f1-110">EXAMPLES</span></span>

### <span data-ttu-id="ff7f1-111">Esempio 1: rimuovere un webhook del registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="ff7f1-112">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="ff7f1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff7f1-113">PARAMETERS</span></span>

### <span data-ttu-id="ff7f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7f1-114">-DefaultProfile</span></span>
<span data-ttu-id="ff7f1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff7f1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff7f1-116">-Name</span></span>
<span data-ttu-id="ff7f1-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-117">Webhook Name.</span></span>

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

### <span data-ttu-id="ff7f1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff7f1-118">-PassThru</span></span>
<span data-ttu-id="ff7f1-119">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="ff7f1-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ff7f1-120">-RegistryName</span></span>
<span data-ttu-id="ff7f1-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="ff7f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff7f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff7f1-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff7f1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff7f1-124">-ResourceId</span></span>
<span data-ttu-id="ff7f1-125">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="ff7f1-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="ff7f1-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-126">-Webhook</span></span>
<span data-ttu-id="ff7f1-127">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="ff7f1-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff7f1-128">-Confirm</span></span>
<span data-ttu-id="ff7f1-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff7f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff7f1-130">-WhatIf</span></span>
<span data-ttu-id="ff7f1-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff7f1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff7f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7f1-133">CommonParameters</span></span>
<span data-ttu-id="ff7f1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7f1-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff7f1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7f1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff7f1-136">INPUTS</span></span>

### <span data-ttu-id="ff7f1-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="ff7f1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ff7f1-138">System.String</span></span>

## <span data-ttu-id="ff7f1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff7f1-139">OUTPUTS</span></span>

### <span data-ttu-id="ff7f1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff7f1-140">System.Boolean</span></span>

## <span data-ttu-id="ff7f1-141">Note</span><span class="sxs-lookup"><span data-stu-id="ff7f1-141">NOTES</span></span>

## <span data-ttu-id="ff7f1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff7f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff7f1-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ff7f1-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ff7f1-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ff7f1-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff7f1-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)