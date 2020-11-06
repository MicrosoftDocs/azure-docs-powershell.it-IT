---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 058c923528227e05a4c8b8078f4495c56edfe20c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509939"
---
# <span data-ttu-id="0073d-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0073d-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="0073d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0073d-102">SYNOPSIS</span></span>
<span data-ttu-id="0073d-103">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0073d-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0073d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0073d-104">SYNTAX</span></span>

### <span data-ttu-id="0073d-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0073d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0073d-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0073d-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0073d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0073d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0073d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0073d-108">DESCRIPTION</span></span>
<span data-ttu-id="0073d-109">Il cmdlet Remove-AzureRmContainerRegistryWebhook rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0073d-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="0073d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0073d-110">EXAMPLES</span></span>

### <span data-ttu-id="0073d-111">Esempio 1: rimuovere un webhook del registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0073d-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="0073d-112">Rimuove un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0073d-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="0073d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0073d-113">PARAMETERS</span></span>

### <span data-ttu-id="0073d-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0073d-114">-Confirm</span></span>
<span data-ttu-id="0073d-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0073d-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0073d-116">-DefaultProfile</span></span>
<span data-ttu-id="0073d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0073d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0073d-118">-Name</span></span>
<span data-ttu-id="0073d-119">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="0073d-119">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0073d-120">-RegistryName</span></span>
<span data-ttu-id="0073d-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0073d-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0073d-122">-ResourceGroupName</span></span>
<span data-ttu-id="0073d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0073d-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0073d-124">-ResourceId</span></span>
<span data-ttu-id="0073d-125">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="0073d-125">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="0073d-126">-Webhook</span></span>
<span data-ttu-id="0073d-127">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0073d-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0073d-128">-WhatIf</span></span>
<span data-ttu-id="0073d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0073d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0073d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0073d-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0073d-131">-PassThru</span></span>
<span data-ttu-id="0073d-132">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="0073d-132">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0073d-133">CommonParameters</span></span>
<span data-ttu-id="0073d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0073d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0073d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0073d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0073d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0073d-136">INPUTS</span></span>

### <span data-ttu-id="0073d-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0073d-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="0073d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0073d-138">System.String</span></span>

## <span data-ttu-id="0073d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0073d-139">OUTPUTS</span></span>

### <span data-ttu-id="0073d-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="0073d-140">System.Object</span></span>

## <span data-ttu-id="0073d-141">Note</span><span class="sxs-lookup"><span data-stu-id="0073d-141">NOTES</span></span>

## <span data-ttu-id="0073d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0073d-142">RELATED LINKS</span></span>

[<span data-ttu-id="0073d-143">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0073d-143">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0073d-144">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0073d-144">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0073d-145">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0073d-145">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0073d-146">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0073d-146">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
