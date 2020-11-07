---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687617"
---
# <span data-ttu-id="70d1e-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="70d1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="70d1e-103">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="70d1e-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70d1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70d1e-104">SYNTAX</span></span>

### <span data-ttu-id="70d1e-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70d1e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d1e-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70d1e-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d1e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70d1e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d1e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70d1e-108">DESCRIPTION</span></span>
<span data-ttu-id="70d1e-109">Il cmdlet Remove-AzureRmContainerRegistryWebhook rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="70d1e-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="70d1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70d1e-110">EXAMPLES</span></span>

### <span data-ttu-id="70d1e-111">Esempio 1: rimuovere un webhook del registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="70d1e-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="70d1e-112">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="70d1e-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="70d1e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70d1e-113">PARAMETERS</span></span>

### <span data-ttu-id="70d1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d1e-114">-DefaultProfile</span></span>
<span data-ttu-id="70d1e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70d1e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70d1e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="70d1e-116">-Name</span></span>
<span data-ttu-id="70d1e-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="70d1e-117">Webhook Name.</span></span>

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

### <span data-ttu-id="70d1e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70d1e-118">-PassThru</span></span>
<span data-ttu-id="70d1e-119">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="70d1e-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="70d1e-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="70d1e-120">-RegistryName</span></span>
<span data-ttu-id="70d1e-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="70d1e-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="70d1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="70d1e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70d1e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="70d1e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70d1e-124">-ResourceId</span></span>
<span data-ttu-id="70d1e-125">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="70d1e-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="70d1e-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-126">-Webhook</span></span>
<span data-ttu-id="70d1e-127">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="70d1e-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="70d1e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70d1e-128">-Confirm</span></span>
<span data-ttu-id="70d1e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70d1e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d1e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d1e-130">-WhatIf</span></span>
<span data-ttu-id="70d1e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70d1e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d1e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70d1e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d1e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d1e-133">CommonParameters</span></span>
<span data-ttu-id="70d1e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d1e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d1e-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d1e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d1e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70d1e-136">INPUTS</span></span>

### <span data-ttu-id="70d1e-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="70d1e-138">Parametri: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70d1e-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="70d1e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70d1e-139">System.String</span></span>

## <span data-ttu-id="70d1e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70d1e-140">OUTPUTS</span></span>

### <span data-ttu-id="70d1e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70d1e-141">System.Boolean</span></span>

## <span data-ttu-id="70d1e-142">Note</span><span class="sxs-lookup"><span data-stu-id="70d1e-142">NOTES</span></span>

## <span data-ttu-id="70d1e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70d1e-143">RELATED LINKS</span></span>

[<span data-ttu-id="70d1e-144">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="70d1e-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="70d1e-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="70d1e-147">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="70d1e-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
