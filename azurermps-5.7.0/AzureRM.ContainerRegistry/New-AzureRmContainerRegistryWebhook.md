---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516828"
---
# <span data-ttu-id="9289d-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9289d-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="9289d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9289d-102">SYNOPSIS</span></span>
<span data-ttu-id="9289d-103">Crea un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="9289d-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9289d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9289d-104">SYNTAX</span></span>

### <span data-ttu-id="9289d-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9289d-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9289d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9289d-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9289d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9289d-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9289d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9289d-108">DESCRIPTION</span></span>
<span data-ttu-id="9289d-109">Il cmdlet New-AzureRmContainerRegistryWebhook crea un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="9289d-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="9289d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9289d-110">EXAMPLES</span></span>

### <span data-ttu-id="9289d-111">Esempio 1: creare un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="9289d-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="9289d-112">Creare un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="9289d-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="9289d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9289d-113">PARAMETERS</span></span>

### <span data-ttu-id="9289d-114">-Azione</span><span class="sxs-lookup"><span data-stu-id="9289d-114">-Action</span></span>
<span data-ttu-id="9289d-115">Elenco di azioni separate da spazi che attivano il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="9289d-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9289d-116">-Confirm</span></span>
<span data-ttu-id="9289d-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9289d-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9289d-118">-DefaultProfile</span></span>
<span data-ttu-id="9289d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9289d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9289d-120">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="9289d-120">-Header</span></span>
<span data-ttu-id="9289d-121">Intestazioni personalizzate che verranno aggiunte alle notifiche di webhook.</span><span class="sxs-lookup"><span data-stu-id="9289d-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9289d-122">-Location</span></span>
<span data-ttu-id="9289d-123">Posizione webhook.</span><span class="sxs-lookup"><span data-stu-id="9289d-123">Webhook Location.</span></span>
<span data-ttu-id="9289d-124">Impostazione predefinita per il percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9289d-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9289d-125">-Name</span></span>
<span data-ttu-id="9289d-126">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="9289d-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-127">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="9289d-127">-Registry</span></span>
<span data-ttu-id="9289d-128">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="9289d-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-129">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="9289d-129">-RegistryName</span></span>
<span data-ttu-id="9289d-130">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="9289d-130">Container Registry Name.</span></span>

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

### <span data-ttu-id="9289d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9289d-131">-ResourceGroupName</span></span>
<span data-ttu-id="9289d-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9289d-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="9289d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9289d-133">-ResourceId</span></span>
<span data-ttu-id="9289d-134">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="9289d-134">The container registry resource id</span></span>

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

### <span data-ttu-id="9289d-135">-Ambito</span><span class="sxs-lookup"><span data-stu-id="9289d-135">-Scope</span></span>
<span data-ttu-id="9289d-136">Ambito webhook.</span><span class="sxs-lookup"><span data-stu-id="9289d-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="9289d-137">-Status</span></span>
<span data-ttu-id="9289d-138">Stato webhook, il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="9289d-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="9289d-139">-Tag</span></span>
<span data-ttu-id="9289d-140">Tag webhook.</span><span class="sxs-lookup"><span data-stu-id="9289d-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-141">-URI</span><span class="sxs-lookup"><span data-stu-id="9289d-141">-Uri</span></span>
<span data-ttu-id="9289d-142">URI del servizio per il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="9289d-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9289d-143">-WhatIf</span></span>
<span data-ttu-id="9289d-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9289d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9289d-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9289d-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9289d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9289d-146">CommonParameters</span></span>
<span data-ttu-id="9289d-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9289d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9289d-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9289d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9289d-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9289d-149">INPUTS</span></span>

### <span data-ttu-id="9289d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9289d-150">System.String</span></span>

## <span data-ttu-id="9289d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9289d-151">OUTPUTS</span></span>

### <span data-ttu-id="9289d-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9289d-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="9289d-153">Note</span><span class="sxs-lookup"><span data-stu-id="9289d-153">NOTES</span></span>

## <span data-ttu-id="9289d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9289d-154">RELATED LINKS</span></span>

[<span data-ttu-id="9289d-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9289d-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9289d-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9289d-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9289d-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9289d-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9289d-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9289d-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
