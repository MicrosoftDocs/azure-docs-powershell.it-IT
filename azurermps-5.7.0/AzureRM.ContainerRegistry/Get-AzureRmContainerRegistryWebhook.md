---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512683"
---
# <span data-ttu-id="de0d6-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de0d6-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="de0d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="de0d6-103">Ottiene un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de0d6-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de0d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de0d6-104">SYNTAX</span></span>

### <span data-ttu-id="de0d6-105">ListWebhookByNameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de0d6-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de0d6-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="de0d6-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de0d6-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de0d6-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de0d6-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de0d6-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de0d6-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de0d6-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de0d6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de0d6-110">DESCRIPTION</span></span>
<span data-ttu-id="de0d6-111">Il cmdlet Get-AzureRmContainerRegistryWebhook ottiene un webhook specificato di registro del contenitore o di tutti i webhook di un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de0d6-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="de0d6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de0d6-112">EXAMPLES</span></span>

### <span data-ttu-id="de0d6-113">Esempio 1: ottenere un webhook specificato di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="de0d6-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="de0d6-114">Ottenere un webhook specificato di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="de0d6-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="de0d6-115">Esempio 2: ottenere tutti i webhook di un contenitore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="de0d6-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="de0d6-116">Ottenere tutti i webhook di un contenitore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="de0d6-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="de0d6-117">Esempio 3: ottenere un webhook specificato di un registro dei contenitori con i dettagli di configurazione</span><span class="sxs-lookup"><span data-stu-id="de0d6-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="de0d6-118">Ottenere un webhook specificato di un registro dei contenitori con i dettagli di configurazione</span><span class="sxs-lookup"><span data-stu-id="de0d6-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="de0d6-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de0d6-119">PARAMETERS</span></span>

### <span data-ttu-id="de0d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0d6-120">-DefaultProfile</span></span>
<span data-ttu-id="de0d6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de0d6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de0d6-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="de0d6-122">-IncludeConfiguration</span></span>
<span data-ttu-id="de0d6-123">Ottenere le informazioni di configurazione per un webhook.</span><span class="sxs-lookup"><span data-stu-id="de0d6-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="de0d6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="de0d6-124">-Name</span></span>
<span data-ttu-id="de0d6-125">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="de0d6-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0d6-126">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="de0d6-126">-Registry</span></span>
<span data-ttu-id="de0d6-127">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de0d6-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de0d6-128">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="de0d6-128">-RegistryName</span></span>
<span data-ttu-id="de0d6-129">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de0d6-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0d6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0d6-130">-ResourceGroupName</span></span>
<span data-ttu-id="de0d6-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de0d6-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0d6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de0d6-132">-ResourceId</span></span>
<span data-ttu-id="de0d6-133">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="de0d6-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="de0d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0d6-134">CommonParameters</span></span>
<span data-ttu-id="de0d6-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0d6-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de0d6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0d6-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de0d6-137">INPUTS</span></span>

### <span data-ttu-id="de0d6-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de0d6-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="de0d6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="de0d6-139">System.String</span></span>

## <span data-ttu-id="de0d6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de0d6-140">OUTPUTS</span></span>

### <span data-ttu-id="de0d6-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de0d6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="de0d6-142">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook, Microsoft. Azure. Commands. ContainerRegistry, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="de0d6-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de0d6-143">Note</span><span class="sxs-lookup"><span data-stu-id="de0d6-143">NOTES</span></span>

## <span data-ttu-id="de0d6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de0d6-144">RELATED LINKS</span></span>

[<span data-ttu-id="de0d6-145">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de0d6-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="de0d6-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de0d6-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="de0d6-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de0d6-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="de0d6-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de0d6-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
