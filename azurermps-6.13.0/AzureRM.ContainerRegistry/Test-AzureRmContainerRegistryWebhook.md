---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685776"
---
# <span data-ttu-id="f3e9b-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="f3e9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e9b-103">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3e9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3e9b-104">SYNTAX</span></span>

### <span data-ttu-id="f3e9b-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3e9b-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3e9b-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3e9b-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3e9b-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3e9b-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e9b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3e9b-108">DESCRIPTION</span></span>
<span data-ttu-id="f3e9b-109">Il cmdlet Test-AzureRmContainerRegistryWebhook attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="f3e9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3e9b-110">EXAMPLES</span></span>

### <span data-ttu-id="f3e9b-111">Esempio 1: attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="f3e9b-112">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="f3e9b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3e9b-113">PARAMETERS</span></span>

### <span data-ttu-id="f3e9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e9b-114">-DefaultProfile</span></span>
<span data-ttu-id="f3e9b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e9b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3e9b-116">-Name</span></span>
<span data-ttu-id="f3e9b-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-117">Webhook Name.</span></span>

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

### <span data-ttu-id="f3e9b-118">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f3e9b-118">-RegistryName</span></span>
<span data-ttu-id="f3e9b-119">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="f3e9b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e9b-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3e9b-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="f3e9b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3e9b-122">-ResourceId</span></span>
<span data-ttu-id="f3e9b-123">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f3e9b-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="f3e9b-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-124">-Webhook</span></span>
<span data-ttu-id="f3e9b-125">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="f3e9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e9b-126">CommonParameters</span></span>
<span data-ttu-id="f3e9b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e9b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e9b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e9b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3e9b-129">INPUTS</span></span>

### <span data-ttu-id="f3e9b-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="f3e9b-131">Parametri: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3e9b-131">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="f3e9b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f3e9b-132">System.String</span></span>

## <span data-ttu-id="f3e9b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3e9b-133">OUTPUTS</span></span>

### <span data-ttu-id="f3e9b-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="f3e9b-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="f3e9b-135">Note</span><span class="sxs-lookup"><span data-stu-id="f3e9b-135">NOTES</span></span>

## <span data-ttu-id="f3e9b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3e9b-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3e9b-137">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-137">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f3e9b-138">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-138">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f3e9b-139">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-139">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f3e9b-140">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e9b-140">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
