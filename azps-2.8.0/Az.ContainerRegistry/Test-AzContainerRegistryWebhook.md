---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4d3a6cef78a644f5448b2825b77ef1d2beabac63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675071"
---
# <span data-ttu-id="88408-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="88408-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="88408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88408-102">SYNOPSIS</span></span>
<span data-ttu-id="88408-103">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="88408-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="88408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88408-104">SYNTAX</span></span>

### <span data-ttu-id="88408-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88408-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88408-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="88408-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88408-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88408-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88408-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88408-108">DESCRIPTION</span></span>
<span data-ttu-id="88408-109">Il cmdlet Test-AzContainerRegistryWebhook attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="88408-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="88408-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88408-110">EXAMPLES</span></span>

### <span data-ttu-id="88408-111">Esempio 1: attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="88408-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="88408-112">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="88408-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="88408-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88408-113">PARAMETERS</span></span>

### <span data-ttu-id="88408-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88408-114">-DefaultProfile</span></span>
<span data-ttu-id="88408-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88408-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88408-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="88408-116">-Name</span></span>
<span data-ttu-id="88408-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="88408-117">Webhook Name.</span></span>

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

### <span data-ttu-id="88408-118">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="88408-118">-RegistryName</span></span>
<span data-ttu-id="88408-119">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="88408-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="88408-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88408-120">-ResourceGroupName</span></span>
<span data-ttu-id="88408-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88408-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="88408-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88408-122">-ResourceId</span></span>
<span data-ttu-id="88408-123">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="88408-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="88408-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="88408-124">-Webhook</span></span>
<span data-ttu-id="88408-125">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="88408-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="88408-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88408-126">CommonParameters</span></span>
<span data-ttu-id="88408-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88408-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88408-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88408-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88408-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88408-129">INPUTS</span></span>

### <span data-ttu-id="88408-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="88408-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="88408-131">System. String</span><span class="sxs-lookup"><span data-stu-id="88408-131">System.String</span></span>

## <span data-ttu-id="88408-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88408-132">OUTPUTS</span></span>

### <span data-ttu-id="88408-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="88408-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="88408-134">Note</span><span class="sxs-lookup"><span data-stu-id="88408-134">NOTES</span></span>

## <span data-ttu-id="88408-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88408-135">RELATED LINKS</span></span>

[<span data-ttu-id="88408-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="88408-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="88408-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="88408-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="88408-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="88408-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="88408-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="88408-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)