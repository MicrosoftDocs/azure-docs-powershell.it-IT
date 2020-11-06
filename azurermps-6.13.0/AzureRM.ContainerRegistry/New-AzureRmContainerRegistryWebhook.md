---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 6cee5cc10fc9cbb1af014e2ad500b38111fc3564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507539"
---
# <span data-ttu-id="c6ea9-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c6ea9-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="c6ea9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ea9-103">Crea un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6ea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6ea9-104">SYNTAX</span></span>

### <span data-ttu-id="c6ea9-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6ea9-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ea9-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ea9-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ea9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ea9-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6ea9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="c6ea9-109">Il cmdlet New-AzureRmContainerRegistryWebhook crea un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="c6ea9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6ea9-110">EXAMPLES</span></span>

### <span data-ttu-id="c6ea9-111">Esempio 1: creare un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="c6ea9-112">Creare un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="c6ea9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6ea9-113">PARAMETERS</span></span>

### <span data-ttu-id="c6ea9-114">-Azione</span><span class="sxs-lookup"><span data-stu-id="c6ea9-114">-Action</span></span>
<span data-ttu-id="c6ea9-115">Elenco di azioni separate da spazi che attivano il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="c6ea9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ea9-116">-DefaultProfile</span></span>
<span data-ttu-id="c6ea9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6ea9-118">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6ea9-118">-Header</span></span>
<span data-ttu-id="c6ea9-119">Intestazioni personalizzate che verranno aggiunte alle notifiche di webhook.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="c6ea9-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c6ea9-120">-Location</span></span>
<span data-ttu-id="c6ea9-121">Posizione webhook.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-121">Webhook Location.</span></span>
<span data-ttu-id="c6ea9-122">Impostazione predefinita per il percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="c6ea9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6ea9-123">-Name</span></span>
<span data-ttu-id="c6ea9-124">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-124">Webhook Name.</span></span>

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

### <span data-ttu-id="c6ea9-125">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c6ea9-125">-Registry</span></span>
<span data-ttu-id="c6ea9-126">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="c6ea9-127">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c6ea9-127">-RegistryName</span></span>
<span data-ttu-id="c6ea9-128">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="c6ea9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ea9-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6ea9-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6ea9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6ea9-131">-ResourceId</span></span>
<span data-ttu-id="c6ea9-132">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="c6ea9-132">The container registry resource id</span></span>

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

### <span data-ttu-id="c6ea9-133">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c6ea9-133">-Scope</span></span>
<span data-ttu-id="c6ea9-134">Ambito webhook.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-134">Webhook scope.</span></span>

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

### <span data-ttu-id="c6ea9-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="c6ea9-135">-Status</span></span>
<span data-ttu-id="c6ea9-136">Stato webhook, il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="c6ea9-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="c6ea9-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6ea9-137">-Tag</span></span>
<span data-ttu-id="c6ea9-138">Tag webhook.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-138">Webhook tags.</span></span>

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

### <span data-ttu-id="c6ea9-139">-URI</span><span class="sxs-lookup"><span data-stu-id="c6ea9-139">-Uri</span></span>
<span data-ttu-id="c6ea9-140">URI del servizio per il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="c6ea9-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6ea9-141">-Confirm</span></span>
<span data-ttu-id="c6ea9-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6ea9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ea9-143">-WhatIf</span></span>
<span data-ttu-id="c6ea9-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ea9-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6ea9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ea9-146">CommonParameters</span></span>
<span data-ttu-id="c6ea9-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ea9-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6ea9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ea9-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6ea9-149">INPUTS</span></span>

### <span data-ttu-id="c6ea9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c6ea9-150">System.String</span></span>

## <span data-ttu-id="c6ea9-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6ea9-151">OUTPUTS</span></span>

### <span data-ttu-id="c6ea9-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c6ea9-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="c6ea9-153">Note</span><span class="sxs-lookup"><span data-stu-id="c6ea9-153">NOTES</span></span>

## <span data-ttu-id="c6ea9-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6ea9-154">RELATED LINKS</span></span>

[<span data-ttu-id="c6ea9-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c6ea9-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c6ea9-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c6ea9-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c6ea9-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c6ea9-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c6ea9-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c6ea9-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
