---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516808"
---
# <span data-ttu-id="14c66-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="14c66-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="14c66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14c66-102">SYNOPSIS</span></span>
<span data-ttu-id="14c66-103">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="14c66-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14c66-104">SYNTAX</span></span>

### <span data-ttu-id="14c66-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14c66-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14c66-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c66-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c66-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c66-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c66-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14c66-108">DESCRIPTION</span></span>
<span data-ttu-id="14c66-109">Il cmdlet Test-AzureRmContainerRegistryWebhook attiva un evento ping webhook.</span><span class="sxs-lookup"><span data-stu-id="14c66-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="14c66-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14c66-110">EXAMPLES</span></span>

### <span data-ttu-id="14c66-111">Esempio 1: attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="14c66-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="14c66-112">Attiva un evento ping di webhook.</span><span class="sxs-lookup"><span data-stu-id="14c66-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="14c66-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14c66-113">PARAMETERS</span></span>

### <span data-ttu-id="14c66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c66-114">-DefaultProfile</span></span>
<span data-ttu-id="14c66-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14c66-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14c66-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="14c66-116">-Name</span></span>
<span data-ttu-id="14c66-117">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="14c66-117">Webhook Name.</span></span>

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

### <span data-ttu-id="14c66-118">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="14c66-118">-RegistryName</span></span>
<span data-ttu-id="14c66-119">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="14c66-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="14c66-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c66-120">-ResourceGroupName</span></span>
<span data-ttu-id="14c66-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14c66-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="14c66-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14c66-122">-ResourceId</span></span>
<span data-ttu-id="14c66-123">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="14c66-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="14c66-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="14c66-124">-Webhook</span></span>
<span data-ttu-id="14c66-125">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="14c66-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="14c66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c66-126">CommonParameters</span></span>
<span data-ttu-id="14c66-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c66-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c66-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c66-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14c66-129">INPUTS</span></span>

### <span data-ttu-id="14c66-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="14c66-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="14c66-131">System. String</span><span class="sxs-lookup"><span data-stu-id="14c66-131">System.String</span></span>

## <span data-ttu-id="14c66-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14c66-132">OUTPUTS</span></span>

### <span data-ttu-id="14c66-133">Microsoft. Azure. Management. ContainerRegistry. Models. EventInfo</span><span class="sxs-lookup"><span data-stu-id="14c66-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="14c66-134">Note</span><span class="sxs-lookup"><span data-stu-id="14c66-134">NOTES</span></span>

## <span data-ttu-id="14c66-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14c66-135">RELATED LINKS</span></span>

[<span data-ttu-id="14c66-136">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="14c66-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="14c66-137">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="14c66-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="14c66-138">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="14c66-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="14c66-139">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="14c66-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
