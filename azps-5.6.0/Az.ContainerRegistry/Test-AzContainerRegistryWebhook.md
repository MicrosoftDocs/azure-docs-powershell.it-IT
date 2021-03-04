---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 837e0fa40bc07ce5c38d6dfd4b7c86efe2425be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956333"
---
# <span data-ttu-id="7bb3e-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="7bb3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb3e-103">Attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="7bb3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bb3e-104">SYNTAX</span></span>

### <span data-ttu-id="7bb3e-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7bb3e-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb3e-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb3e-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bb3e-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb3e-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bb3e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7bb3e-108">DESCRIPTION</span></span>
<span data-ttu-id="7bb3e-109">Il cmdlet Test-AzContainerRegistryWebhook attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="7bb3e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bb3e-110">EXAMPLES</span></span>

### <span data-ttu-id="7bb3e-111">Esempio 1: attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="7bb3e-112">Attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="7bb3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bb3e-113">PARAMETERS</span></span>

### <span data-ttu-id="7bb3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb3e-114">-DefaultProfile</span></span>
<span data-ttu-id="7bb3e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb3e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7bb3e-116">-Name</span></span>
<span data-ttu-id="7bb3e-117">Nome Webhook.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-117">Webhook Name.</span></span>

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

### <span data-ttu-id="7bb3e-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7bb3e-118">-RegistryName</span></span>
<span data-ttu-id="7bb3e-119">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="7bb3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bb3e-121">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="7bb3e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bb3e-122">-ResourceId</span></span>
<span data-ttu-id="7bb3e-123">ID risorsa Webhook del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="7bb3e-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="7bb3e-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-124">-Webhook</span></span>
<span data-ttu-id="7bb3e-125">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="7bb3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb3e-126">CommonParameters</span></span>
<span data-ttu-id="7bb3e-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb3e-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7bb3e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb3e-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="7bb3e-129">INPUTS</span></span>

### <span data-ttu-id="7bb3e-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="7bb3e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7bb3e-131">System.String</span></span>

## <span data-ttu-id="7bb3e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bb3e-132">OUTPUTS</span></span>

### <span data-ttu-id="7bb3e-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="7bb3e-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="7bb3e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="7bb3e-134">NOTES</span></span>

## <span data-ttu-id="7bb3e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bb3e-135">RELATED LINKS</span></span>

[<span data-ttu-id="7bb3e-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7bb3e-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7bb3e-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7bb3e-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7bb3e-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)