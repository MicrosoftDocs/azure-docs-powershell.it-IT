---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 10acca5a89c4ea84d475e5eea2e89e18942116f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975454"
---
# <span data-ttu-id="608cf-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="608cf-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="608cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608cf-102">SYNOPSIS</span></span>
<span data-ttu-id="608cf-103">Crea un webhook del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="608cf-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="608cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="608cf-104">SYNTAX</span></span>

### <span data-ttu-id="608cf-105">NameResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="608cf-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="608cf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="608cf-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608cf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="608cf-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="608cf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="608cf-108">DESCRIPTION</span></span>
<span data-ttu-id="608cf-109">Il cmdlet New-AzContainerRegistryWebhook crea un webhook del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="608cf-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="608cf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="608cf-110">EXAMPLES</span></span>

### <span data-ttu-id="608cf-111">Esempio 1: Creare un webhook contenitore del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="608cf-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="608cf-112">Creare un webhook del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="608cf-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="608cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="608cf-113">PARAMETERS</span></span>

### <span data-ttu-id="608cf-114">-Action</span><span class="sxs-lookup"><span data-stu-id="608cf-114">-Action</span></span>
<span data-ttu-id="608cf-115">Elenco di azioni separate da spazi che attivano l'invio di notifiche al WebHook.</span><span class="sxs-lookup"><span data-stu-id="608cf-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608cf-116">-DefaultProfile</span></span>
<span data-ttu-id="608cf-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="608cf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="608cf-118">-Header</span><span class="sxs-lookup"><span data-stu-id="608cf-118">-Header</span></span>
<span data-ttu-id="608cf-119">Intestazioni personalizzate che verranno aggiunte alle notifiche webhook.</span><span class="sxs-lookup"><span data-stu-id="608cf-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-120">-Location</span><span class="sxs-lookup"><span data-stu-id="608cf-120">-Location</span></span>
<span data-ttu-id="608cf-121">Posizione Webhook.</span><span class="sxs-lookup"><span data-stu-id="608cf-121">Webhook Location.</span></span>
<span data-ttu-id="608cf-122">Per impostazione predefinita, viene selezionata la posizione del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="608cf-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="608cf-123">-Name</span></span>
<span data-ttu-id="608cf-124">Nome Webhook.</span><span class="sxs-lookup"><span data-stu-id="608cf-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="608cf-125">-Registry</span></span>
<span data-ttu-id="608cf-126">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="608cf-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="608cf-127">-RegistryName</span></span>
<span data-ttu-id="608cf-128">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="608cf-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="608cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="608cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="608cf-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="608cf-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="608cf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="608cf-131">-ResourceId</span></span>
<span data-ttu-id="608cf-132">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="608cf-132">The container registry resource id</span></span>

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

### <span data-ttu-id="608cf-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="608cf-133">-Scope</span></span>
<span data-ttu-id="608cf-134">Ambito Webhook.</span><span class="sxs-lookup"><span data-stu-id="608cf-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="608cf-135">-Status</span></span>
<span data-ttu-id="608cf-136">Stato Webhook, il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="608cf-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="608cf-137">-Tag</span></span>
<span data-ttu-id="608cf-138">Tag Webhook.</span><span class="sxs-lookup"><span data-stu-id="608cf-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="608cf-139">-Uri</span></span>
<span data-ttu-id="608cf-140">URI del servizio per il Webhook in cui pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="608cf-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608cf-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="608cf-141">-Confirm</span></span>
<span data-ttu-id="608cf-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="608cf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608cf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608cf-143">-WhatIf</span></span>
<span data-ttu-id="608cf-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="608cf-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="608cf-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="608cf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608cf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608cf-146">CommonParameters</span></span>
<span data-ttu-id="608cf-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608cf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608cf-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="608cf-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608cf-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="608cf-149">INPUTS</span></span>

### <span data-ttu-id="608cf-150">System.String</span><span class="sxs-lookup"><span data-stu-id="608cf-150">System.String</span></span>

## <span data-ttu-id="608cf-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="608cf-151">OUTPUTS</span></span>

### <span data-ttu-id="608cf-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="608cf-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="608cf-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="608cf-153">NOTES</span></span>

## <span data-ttu-id="608cf-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="608cf-154">RELATED LINKS</span></span>

[<span data-ttu-id="608cf-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="608cf-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="608cf-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="608cf-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="608cf-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="608cf-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="608cf-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="608cf-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)