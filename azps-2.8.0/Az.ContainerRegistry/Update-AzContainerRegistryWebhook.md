---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 79cb62f7a80e06a811ce6c0b2f7ff8f23005d39a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675065"
---
# <span data-ttu-id="36af4-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="36af4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36af4-102">SYNOPSIS</span></span>
<span data-ttu-id="36af4-103">Aggiorna un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="36af4-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="36af4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36af4-104">SYNTAX</span></span>

### <span data-ttu-id="36af4-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36af4-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36af4-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="36af4-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36af4-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36af4-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36af4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36af4-108">DESCRIPTION</span></span>
<span data-ttu-id="36af4-109">Il cmdlet Update-AzContainerRegistryWebhook aggiorna un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="36af4-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="36af4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36af4-110">EXAMPLES</span></span>

### <span data-ttu-id="36af4-111">Esempio 1: aggiornare un webhook del registro di sistema del contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="36af4-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="36af4-112">Aggiornare un webhook del registro di sistema del contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="36af4-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="36af4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36af4-113">PARAMETERS</span></span>

### <span data-ttu-id="36af4-114">-Azione</span><span class="sxs-lookup"><span data-stu-id="36af4-114">-Action</span></span>
<span data-ttu-id="36af4-115">Elenco di azioni separate da spazi che attivano il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="36af4-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="36af4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36af4-116">-DefaultProfile</span></span>
<span data-ttu-id="36af4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36af4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36af4-118">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="36af4-118">-Header</span></span>
<span data-ttu-id="36af4-119">Intestazioni personalizzate separate da spazi in formato "Key \[ = valore \] " che verranno aggiunte alle notifiche di webhook.</span><span class="sxs-lookup"><span data-stu-id="36af4-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="36af4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="36af4-120">-Name</span></span>
<span data-ttu-id="36af4-121">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="36af4-121">Webhook Name.</span></span>

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

### <span data-ttu-id="36af4-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="36af4-122">-RegistryName</span></span>
<span data-ttu-id="36af4-123">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="36af4-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="36af4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36af4-124">-ResourceGroupName</span></span>
<span data-ttu-id="36af4-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36af4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="36af4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36af4-126">-ResourceId</span></span>
<span data-ttu-id="36af4-127">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="36af4-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="36af4-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="36af4-128">-Scope</span></span>
<span data-ttu-id="36af4-129">Ambito webhook.</span><span class="sxs-lookup"><span data-stu-id="36af4-129">Webhook scope.</span></span>

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

### <span data-ttu-id="36af4-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="36af4-130">-Status</span></span>
<span data-ttu-id="36af4-131">Stato del webhook</span><span class="sxs-lookup"><span data-stu-id="36af4-131">Webhook status</span></span>

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

### <span data-ttu-id="36af4-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="36af4-132">-Tag</span></span>
<span data-ttu-id="36af4-133">Spaziatura con tag separati nel \[ formato "Key = valore \] ".</span><span class="sxs-lookup"><span data-stu-id="36af4-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="36af4-134">-URI</span><span class="sxs-lookup"><span data-stu-id="36af4-134">-Uri</span></span>
<span data-ttu-id="36af4-135">URI del servizio per il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="36af4-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="36af4-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="36af4-136">-Webhook</span></span>
<span data-ttu-id="36af4-137">Oggetto webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="36af4-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="36af4-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36af4-138">-Confirm</span></span>
<span data-ttu-id="36af4-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36af4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36af4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36af4-140">-WhatIf</span></span>
<span data-ttu-id="36af4-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36af4-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36af4-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36af4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36af4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36af4-143">CommonParameters</span></span>
<span data-ttu-id="36af4-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36af4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36af4-145">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36af4-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36af4-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36af4-146">INPUTS</span></span>

### <span data-ttu-id="36af4-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="36af4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="36af4-148">System.String</span></span>

## <span data-ttu-id="36af4-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36af4-149">OUTPUTS</span></span>

### <span data-ttu-id="36af4-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="36af4-151">Note</span><span class="sxs-lookup"><span data-stu-id="36af4-151">NOTES</span></span>

## <span data-ttu-id="36af4-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36af4-152">RELATED LINKS</span></span>

[<span data-ttu-id="36af4-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="36af4-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="36af4-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="36af4-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="36af4-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)