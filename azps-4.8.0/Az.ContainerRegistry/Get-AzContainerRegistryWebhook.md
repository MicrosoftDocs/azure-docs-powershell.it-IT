---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190842"
---
# <span data-ttu-id="84324-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="84324-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="84324-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84324-102">SYNOPSIS</span></span>
<span data-ttu-id="84324-103">Ottiene un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="84324-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="84324-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84324-104">SYNTAX</span></span>

### <span data-ttu-id="84324-105">ListWebhookByNameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84324-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84324-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="84324-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84324-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84324-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84324-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84324-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84324-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84324-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84324-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84324-110">DESCRIPTION</span></span>
<span data-ttu-id="84324-111">Il cmdlet Get-AzContainerRegistryWebhook ottiene un webhook specificato di registro del contenitore o di tutti i webhook di un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="84324-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="84324-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84324-112">EXAMPLES</span></span>

### <span data-ttu-id="84324-113">Esempio 1: ottenere un webhook specificato di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="84324-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="84324-114">Ottenere un webhook specificato di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="84324-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="84324-115">Esempio 2: ottenere tutti i webhook di un contenitore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="84324-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="84324-116">Ottenere tutti i webhook di un contenitore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="84324-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="84324-117">Esempio 3: ottenere un webhook specificato di un registro dei contenitori con i dettagli di configurazione</span><span class="sxs-lookup"><span data-stu-id="84324-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="84324-118">Ottenere un webhook specificato di un registro dei contenitori con i dettagli di configurazione</span><span class="sxs-lookup"><span data-stu-id="84324-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="84324-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84324-119">PARAMETERS</span></span>

### <span data-ttu-id="84324-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84324-120">-DefaultProfile</span></span>
<span data-ttu-id="84324-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84324-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84324-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="84324-122">-IncludeConfiguration</span></span>
<span data-ttu-id="84324-123">Ottenere le informazioni di configurazione per un webhook.</span><span class="sxs-lookup"><span data-stu-id="84324-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="84324-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="84324-124">-Name</span></span>
<span data-ttu-id="84324-125">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="84324-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84324-126">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="84324-126">-Registry</span></span>
<span data-ttu-id="84324-127">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="84324-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84324-128">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="84324-128">-RegistryName</span></span>
<span data-ttu-id="84324-129">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="84324-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84324-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84324-130">-ResourceGroupName</span></span>
<span data-ttu-id="84324-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84324-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84324-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84324-132">-ResourceId</span></span>
<span data-ttu-id="84324-133">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="84324-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="84324-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84324-134">CommonParameters</span></span>
<span data-ttu-id="84324-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84324-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84324-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84324-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84324-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84324-137">INPUTS</span></span>

### <span data-ttu-id="84324-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84324-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="84324-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84324-139">System.String</span></span>

## <span data-ttu-id="84324-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84324-140">OUTPUTS</span></span>

### <span data-ttu-id="84324-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="84324-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="84324-142">Note</span><span class="sxs-lookup"><span data-stu-id="84324-142">NOTES</span></span>

## <span data-ttu-id="84324-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84324-143">RELATED LINKS</span></span>

[<span data-ttu-id="84324-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="84324-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="84324-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="84324-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="84324-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="84324-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="84324-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="84324-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)