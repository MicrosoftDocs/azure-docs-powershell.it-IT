---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 36bc713561c739804b358e4b778e17740bd9fb6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977470"
---
# <span data-ttu-id="242c6-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="242c6-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="242c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="242c6-102">SYNOPSIS</span></span>
<span data-ttu-id="242c6-103">Ottiene un webhook del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="242c6-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="242c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="242c6-104">SYNTAX</span></span>

### <span data-ttu-id="242c6-105">ListWebhookByNameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="242c6-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="242c6-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="242c6-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="242c6-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="242c6-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="242c6-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="242c6-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="242c6-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="242c6-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="242c6-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="242c6-110">DESCRIPTION</span></span>
<span data-ttu-id="242c6-111">Il Get-AzContainerRegistryWebhook cmdlet ottiene un webhook specificato del Registro di sistema del contenitore o tutti gli webhook di un registro contenitore.</span><span class="sxs-lookup"><span data-stu-id="242c6-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="242c6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="242c6-112">EXAMPLES</span></span>

### <span data-ttu-id="242c6-113">Esempio 1: Ottenere un webhook specificato di un Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="242c6-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="242c6-114">Ottenere un webhook specificato di un Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="242c6-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="242c6-115">Esempio 2: Ottenere tutti gli oggetti Web di un Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="242c6-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="242c6-116">Ottenere tutti gli oggetti Web di un Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="242c6-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="242c6-117">Esempio 3: Ottenere un webhook specificato di un Registro di sistema contenitore con dettagli di configurazione</span><span class="sxs-lookup"><span data-stu-id="242c6-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="242c6-118">Ottenere un webhook specificato di un Registro di sistema contenitore con dettagli di configurazione</span><span class="sxs-lookup"><span data-stu-id="242c6-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="242c6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="242c6-119">PARAMETERS</span></span>

### <span data-ttu-id="242c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="242c6-120">-DefaultProfile</span></span>
<span data-ttu-id="242c6-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="242c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="242c6-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="242c6-122">-IncludeConfiguration</span></span>
<span data-ttu-id="242c6-123">Ottenere le informazioni di configurazione per un webhook.</span><span class="sxs-lookup"><span data-stu-id="242c6-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="242c6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="242c6-124">-Name</span></span>
<span data-ttu-id="242c6-125">Nome Webhook.</span><span class="sxs-lookup"><span data-stu-id="242c6-125">Webhook Name.</span></span>

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

### <span data-ttu-id="242c6-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="242c6-126">-Registry</span></span>
<span data-ttu-id="242c6-127">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="242c6-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="242c6-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="242c6-128">-RegistryName</span></span>
<span data-ttu-id="242c6-129">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="242c6-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="242c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="242c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="242c6-131">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="242c6-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="242c6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="242c6-132">-ResourceId</span></span>
<span data-ttu-id="242c6-133">ID risorsa Webhook del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="242c6-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="242c6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="242c6-134">CommonParameters</span></span>
<span data-ttu-id="242c6-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="242c6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="242c6-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="242c6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="242c6-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="242c6-137">INPUTS</span></span>

### <span data-ttu-id="242c6-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="242c6-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="242c6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="242c6-139">System.String</span></span>

## <span data-ttu-id="242c6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="242c6-140">OUTPUTS</span></span>

### <span data-ttu-id="242c6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="242c6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="242c6-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="242c6-142">NOTES</span></span>

## <span data-ttu-id="242c6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="242c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="242c6-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="242c6-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="242c6-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="242c6-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="242c6-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="242c6-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="242c6-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="242c6-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)