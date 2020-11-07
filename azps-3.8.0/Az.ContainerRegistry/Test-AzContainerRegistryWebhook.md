---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864512"
---
# <span data-ttu-id="f9d49-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="f9d49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9d49-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d49-103">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="f9d49-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="f9d49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9d49-104">SYNTAX</span></span>

### <span data-ttu-id="f9d49-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9d49-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9d49-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d49-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9d49-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d49-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9d49-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9d49-108">DESCRIPTION</span></span>
<span data-ttu-id="f9d49-109">Il cmdlet Test-AzContainerRegistryWebhook attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="f9d49-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="f9d49-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9d49-110">EXAMPLES</span></span>

### <span data-ttu-id="f9d49-111">Esempio 1: attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="f9d49-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="f9d49-112">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="f9d49-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="f9d49-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9d49-113">PARAMETERS</span></span>

### <span data-ttu-id="f9d49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d49-114">-DefaultProfile</span></span>
<span data-ttu-id="f9d49-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9d49-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9d49-116">-Name</span></span>
<span data-ttu-id="f9d49-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="f9d49-117">Webhook Name.</span></span>

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

### <span data-ttu-id="f9d49-118">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f9d49-118">-RegistryName</span></span>
<span data-ttu-id="f9d49-119">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f9d49-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="f9d49-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d49-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9d49-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9d49-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9d49-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d49-122">-ResourceId</span></span>
<span data-ttu-id="f9d49-123">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f9d49-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="f9d49-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-124">-Webhook</span></span>
<span data-ttu-id="f9d49-125">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f9d49-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="f9d49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d49-126">CommonParameters</span></span>
<span data-ttu-id="f9d49-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d49-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9d49-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d49-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9d49-129">INPUTS</span></span>

### <span data-ttu-id="f9d49-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="f9d49-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f9d49-131">System.String</span></span>

## <span data-ttu-id="f9d49-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9d49-132">OUTPUTS</span></span>

### <span data-ttu-id="f9d49-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="f9d49-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="f9d49-134">Note</span><span class="sxs-lookup"><span data-stu-id="f9d49-134">NOTES</span></span>

## <span data-ttu-id="f9d49-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9d49-135">RELATED LINKS</span></span>

[<span data-ttu-id="f9d49-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f9d49-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f9d49-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f9d49-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9d49-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)