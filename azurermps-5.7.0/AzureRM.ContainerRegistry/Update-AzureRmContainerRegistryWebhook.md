---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 7515046ed6e9fd6ba5c64b8123f8113b28b53f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686208"
---
# <span data-ttu-id="ff5b7-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="ff5b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5b7-103">Aggiorna un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff5b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-104">SYNTAX</span></span>

### <span data-ttu-id="ff5b7-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff5b7-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff5b7-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff5b7-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff5b7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff5b7-108">DESCRIPTION</span></span>
<span data-ttu-id="ff5b7-109">Il cmdlet Update-AzureRmContainerRegistryWebhook aggiorna un webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="ff5b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-110">EXAMPLES</span></span>

### <span data-ttu-id="ff5b7-111">Esempio 1: aggiornare un webhook del registro di sistema del contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="ff5b7-112">Aggiornare un webhook del registro di sistema del contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="ff5b7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-113">PARAMETERS</span></span>

### <span data-ttu-id="ff5b7-114">-Azione</span><span class="sxs-lookup"><span data-stu-id="ff5b7-114">-Action</span></span>
<span data-ttu-id="ff5b7-115">Elenco di azioni separate da spazi che attivano il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5b7-116">-DefaultProfile</span></span>
<span data-ttu-id="ff5b7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff5b7-118">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff5b7-118">-Header</span></span>
<span data-ttu-id="ff5b7-119">Intestazioni personalizzate separate da spazi in formato "Key \[ = valore \] " che verranno aggiunte alle notifiche di webhook.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="ff5b7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff5b7-120">-Name</span></span>
<span data-ttu-id="ff5b7-121">Nome webhook.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-121">Webhook Name.</span></span>

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

### <span data-ttu-id="ff5b7-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ff5b7-122">-RegistryName</span></span>
<span data-ttu-id="ff5b7-123">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="ff5b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff5b7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff5b7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff5b7-126">-ResourceId</span></span>
<span data-ttu-id="ff5b7-127">ID risorsa webhook del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="ff5b7-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="ff5b7-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="ff5b7-128">-Scope</span></span>
<span data-ttu-id="ff5b7-129">Ambito webhook.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-129">Webhook scope.</span></span>

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

### <span data-ttu-id="ff5b7-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="ff5b7-130">-Status</span></span>
<span data-ttu-id="ff5b7-131">Stato del webhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-131">Webhook status</span></span>

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

### <span data-ttu-id="ff5b7-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff5b7-132">-Tag</span></span>
<span data-ttu-id="ff5b7-133">Spaziatura con tag separati nel \[ formato "Key = valore \] ".</span><span class="sxs-lookup"><span data-stu-id="ff5b7-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="ff5b7-134">-URI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-134">-Uri</span></span>
<span data-ttu-id="ff5b7-135">URI del servizio per il webhook per pubblicare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5b7-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-136">-Webhook</span></span>
<span data-ttu-id="ff5b7-137">Oggetto webhook del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="ff5b7-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff5b7-138">-Confirm</span></span>
<span data-ttu-id="ff5b7-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff5b7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff5b7-140">-WhatIf</span></span>
<span data-ttu-id="ff5b7-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff5b7-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff5b7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5b7-143">CommonParameters</span></span>
<span data-ttu-id="ff5b7-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5b7-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5b7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5b7-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-146">INPUTS</span></span>

### <span data-ttu-id="ff5b7-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="ff5b7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ff5b7-148">System.String</span></span>

## <span data-ttu-id="ff5b7-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff5b7-149">OUTPUTS</span></span>

### <span data-ttu-id="ff5b7-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="ff5b7-151">Note</span><span class="sxs-lookup"><span data-stu-id="ff5b7-151">NOTES</span></span>

## <span data-ttu-id="ff5b7-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-152">RELATED LINKS</span></span>

[<span data-ttu-id="ff5b7-153">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-153">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="ff5b7-154">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-154">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="ff5b7-155">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-155">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="ff5b7-156">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ff5b7-156">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
