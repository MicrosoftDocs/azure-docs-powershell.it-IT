---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032543"
---
# <span data-ttu-id="494b2-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="494b2-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="494b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="494b2-102">SYNOPSIS</span></span>
<span data-ttu-id="494b2-103">Crea un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="494b2-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="494b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="494b2-104">SYNTAX</span></span>

### <span data-ttu-id="494b2-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="494b2-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="494b2-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="494b2-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="494b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="494b2-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="494b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="494b2-108">DESCRIPTION</span></span>
<span data-ttu-id="494b2-109">Il cmdlet New-AzContainerRegistryWebhook crea un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="494b2-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="494b2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="494b2-110">EXAMPLES</span></span>

### <span data-ttu-id="494b2-111">Esempio 1: creare un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="494b2-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="494b2-112">Creare un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="494b2-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="494b2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="494b2-113">PARAMETERS</span></span>

### <span data-ttu-id="494b2-114">-Azione</span><span class="sxs-lookup"><span data-stu-id="494b2-114">-Action</span></span>
<span data-ttu-id="494b2-115">Elenco di azioni separate da spazi che attivano il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="494b2-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="494b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="494b2-116">-DefaultProfile</span></span>
<span data-ttu-id="494b2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="494b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="494b2-118">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="494b2-118">-Header</span></span>
<span data-ttu-id="494b2-119">Intestazioni personalizzate che verranno aggiunte alle notifiche di webhook.</span><span class="sxs-lookup"><span data-stu-id="494b2-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="494b2-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="494b2-120">-Location</span></span>
<span data-ttu-id="494b2-121">Posizione webhook.</span><span class="sxs-lookup"><span data-stu-id="494b2-121">Webhook Location.</span></span>
<span data-ttu-id="494b2-122">Impostazione predefinita per il percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="494b2-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="494b2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="494b2-123">-Name</span></span>
<span data-ttu-id="494b2-124">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="494b2-124">Webhook Name.</span></span>

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

### <span data-ttu-id="494b2-125">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="494b2-125">-Registry</span></span>
<span data-ttu-id="494b2-126">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="494b2-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="494b2-127">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="494b2-127">-RegistryName</span></span>
<span data-ttu-id="494b2-128">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="494b2-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="494b2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="494b2-129">-ResourceGroupName</span></span>
<span data-ttu-id="494b2-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="494b2-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="494b2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="494b2-131">-ResourceId</span></span>
<span data-ttu-id="494b2-132">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="494b2-132">The container registry resource id</span></span>

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

### <span data-ttu-id="494b2-133">-Ambito</span><span class="sxs-lookup"><span data-stu-id="494b2-133">-Scope</span></span>
<span data-ttu-id="494b2-134">Ambito webhook.</span><span class="sxs-lookup"><span data-stu-id="494b2-134">Webhook scope.</span></span>

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

### <span data-ttu-id="494b2-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="494b2-135">-Status</span></span>
<span data-ttu-id="494b2-136">Stato webhook, il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="494b2-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="494b2-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="494b2-137">-Tag</span></span>
<span data-ttu-id="494b2-138">Tag webhook.</span><span class="sxs-lookup"><span data-stu-id="494b2-138">Webhook tags.</span></span>

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

### <span data-ttu-id="494b2-139">-URI</span><span class="sxs-lookup"><span data-stu-id="494b2-139">-Uri</span></span>
<span data-ttu-id="494b2-140">URI del servizio per il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="494b2-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="494b2-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="494b2-141">-Confirm</span></span>
<span data-ttu-id="494b2-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="494b2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="494b2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="494b2-143">-WhatIf</span></span>
<span data-ttu-id="494b2-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="494b2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="494b2-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="494b2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="494b2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="494b2-146">CommonParameters</span></span>
<span data-ttu-id="494b2-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="494b2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="494b2-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="494b2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="494b2-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="494b2-149">INPUTS</span></span>

### <span data-ttu-id="494b2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="494b2-150">System.String</span></span>

## <span data-ttu-id="494b2-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="494b2-151">OUTPUTS</span></span>

### <span data-ttu-id="494b2-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="494b2-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="494b2-153">Note</span><span class="sxs-lookup"><span data-stu-id="494b2-153">NOTES</span></span>

## <span data-ttu-id="494b2-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="494b2-154">RELATED LINKS</span></span>

[<span data-ttu-id="494b2-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="494b2-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="494b2-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="494b2-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="494b2-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="494b2-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="494b2-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="494b2-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)