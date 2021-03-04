---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: cede1001f475d820dfec7131a8c86815bd98adb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956253"
---
# <span data-ttu-id="27072-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="27072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27072-102">SYNOPSIS</span></span>
<span data-ttu-id="27072-103">Aggiorna un webhook del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="27072-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="27072-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27072-104">SYNTAX</span></span>

### <span data-ttu-id="27072-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27072-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27072-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="27072-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27072-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27072-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27072-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27072-108">DESCRIPTION</span></span>
<span data-ttu-id="27072-109">Il Update-AzContainerRegistryWebhook cmdlet aggiorna un webhook del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="27072-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="27072-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27072-110">EXAMPLES</span></span>

### <span data-ttu-id="27072-111">Esempio 1: Aggiornare un webhook del Registro di sistema contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="27072-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="27072-112">Aggiornare un webhook del Registro di sistema contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="27072-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="27072-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27072-113">PARAMETERS</span></span>

### <span data-ttu-id="27072-114">-Action</span><span class="sxs-lookup"><span data-stu-id="27072-114">-Action</span></span>
<span data-ttu-id="27072-115">Elenco di azioni separate da spazi che attivano l'invio di notifiche al WebHook.</span><span class="sxs-lookup"><span data-stu-id="27072-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27072-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27072-116">-DefaultProfile</span></span>
<span data-ttu-id="27072-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27072-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27072-118">-Header</span><span class="sxs-lookup"><span data-stu-id="27072-118">-Header</span></span>
<span data-ttu-id="27072-119">Spaziare le intestazioni personalizzate nel formato 'chiave \[ \] =valore' che verrà aggiunto alle notifiche webhook.</span><span class="sxs-lookup"><span data-stu-id="27072-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="27072-120">-Name</span><span class="sxs-lookup"><span data-stu-id="27072-120">-Name</span></span>
<span data-ttu-id="27072-121">Nome Webhook.</span><span class="sxs-lookup"><span data-stu-id="27072-121">Webhook Name.</span></span>

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

### <span data-ttu-id="27072-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="27072-122">-RegistryName</span></span>
<span data-ttu-id="27072-123">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="27072-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="27072-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27072-124">-ResourceGroupName</span></span>
<span data-ttu-id="27072-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27072-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="27072-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27072-126">-ResourceId</span></span>
<span data-ttu-id="27072-127">ID risorsa Webhook del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="27072-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="27072-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="27072-128">-Scope</span></span>
<span data-ttu-id="27072-129">Ambito Webhook.</span><span class="sxs-lookup"><span data-stu-id="27072-129">Webhook scope.</span></span>

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

### <span data-ttu-id="27072-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="27072-130">-Status</span></span>
<span data-ttu-id="27072-131">Stato Webhook</span><span class="sxs-lookup"><span data-stu-id="27072-131">Webhook status</span></span>

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

### <span data-ttu-id="27072-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="27072-132">-Tag</span></span>
<span data-ttu-id="27072-133">Tag separati da spazi nel formato 'chiave \[ \] =valore'.</span><span class="sxs-lookup"><span data-stu-id="27072-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="27072-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="27072-134">-Uri</span></span>
<span data-ttu-id="27072-135">URI del servizio per il Webhook in cui pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="27072-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27072-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="27072-136">-Webhook</span></span>
<span data-ttu-id="27072-137">Container Registry Webhook Object.</span><span class="sxs-lookup"><span data-stu-id="27072-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="27072-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27072-138">-Confirm</span></span>
<span data-ttu-id="27072-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27072-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27072-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27072-140">-WhatIf</span></span>
<span data-ttu-id="27072-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27072-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27072-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27072-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27072-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27072-143">CommonParameters</span></span>
<span data-ttu-id="27072-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27072-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27072-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27072-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27072-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="27072-146">INPUTS</span></span>

### <span data-ttu-id="27072-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="27072-148">System.String</span><span class="sxs-lookup"><span data-stu-id="27072-148">System.String</span></span>

## <span data-ttu-id="27072-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27072-149">OUTPUTS</span></span>

### <span data-ttu-id="27072-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="27072-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="27072-151">NOTES</span></span>

## <span data-ttu-id="27072-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27072-152">RELATED LINKS</span></span>

[<span data-ttu-id="27072-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="27072-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="27072-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="27072-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="27072-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)