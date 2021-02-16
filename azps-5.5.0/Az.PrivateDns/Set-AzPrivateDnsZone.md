---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179014"
---
# <span data-ttu-id="71076-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="71076-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="71076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71076-102">SYNOPSIS</span></span>
<span data-ttu-id="71076-103">Aggiorna un'area DNS privata da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71076-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="71076-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71076-104">SYNTAX</span></span>

### <span data-ttu-id="71076-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71076-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71076-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="71076-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71076-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="71076-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71076-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71076-108">DESCRIPTION</span></span>
<span data-ttu-id="71076-109">Il cmdlet **Set-AzPrivateDnsZone** aggiorna in modo permanente un'area DNS (Domain Name System) privata da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="71076-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="71076-110">È possibile passare un **oggetto PrivateDnsZone** usando il parametro *PrivateZone* o l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="71076-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="71076-111">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="71076-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="71076-112">Quando si specifica l'area usando un oggetto **PrivateDnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene aggiornata se è stata modificata nel DNS di Azure perché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nella risorsa zona DNS vengono conteggiati come modifiche, non le operazioni sui set di record all'interno dell'area).</span><span class="sxs-lookup"><span data-stu-id="71076-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="71076-113">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="71076-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="71076-114">Questa operazione può essere soppressa con il parametro *Overwrite,* che aggiorna l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="71076-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="71076-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71076-115">EXAMPLES</span></span>

### <span data-ttu-id="71076-116">Esempio 1: Aggiorna un'area privata</span><span class="sxs-lookup"><span data-stu-id="71076-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="71076-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71076-117">PARAMETERS</span></span>

### <span data-ttu-id="71076-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71076-118">-DefaultProfile</span></span>
<span data-ttu-id="71076-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="71076-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71076-120">-Name</span><span class="sxs-lookup"><span data-stu-id="71076-120">-Name</span></span>
<span data-ttu-id="71076-121">Specifica il nome dell'area DNS privata aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71076-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="71076-122">È anche necessario specificare il *parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="71076-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="71076-123">In alternativa, è possibile specificare l'area DNS privata usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="71076-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71076-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="71076-124">-Overwrite</span></span>
<span data-ttu-id="71076-125">Quando si specifica l'area usando un oggetto **PrivateDnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene aggiornata se è stata modificata nel DNS di Azure dopo il recupero dell'oggetto **DnsZone** locale (solo le operazioni direttamente nella risorsa zona DNS vengono conteggiati come modifiche, non le operazioni sui set di record all'interno dell'area).</span><span class="sxs-lookup"><span data-stu-id="71076-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="71076-126">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="71076-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="71076-127">Questa operazione può essere soppressa con il parametro *Overwrite,* che aggiorna l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="71076-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71076-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="71076-128">-PrivateZone</span></span>
<span data-ttu-id="71076-129">L'oggetto area da impostare.</span><span class="sxs-lookup"><span data-stu-id="71076-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71076-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71076-130">-ResourceGroupName</span></span>
<span data-ttu-id="71076-131">Specifica il nome del gruppo di risorse che contiene l'area da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="71076-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="71076-132">È anche necessario specificare il *parametro ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="71076-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="71076-133">In alternativa, è possibile specificare l'area DNS privata usando un **oggetto DnsZone,** passato tramite la pipeline o il parametro *Zone.*</span><span class="sxs-lookup"><span data-stu-id="71076-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71076-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71076-134">-ResourceId</span></span>
<span data-ttu-id="71076-135">ID Risorsa area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="71076-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71076-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="71076-136">-Tag</span></span>
<span data-ttu-id="71076-137">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="71076-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71076-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71076-138">-Confirm</span></span>
<span data-ttu-id="71076-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71076-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71076-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71076-140">-WhatIf</span></span>
<span data-ttu-id="71076-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71076-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71076-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71076-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71076-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71076-143">CommonParameters</span></span>
<span data-ttu-id="71076-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71076-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71076-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71076-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71076-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="71076-146">INPUTS</span></span>

### <span data-ttu-id="71076-147">System.String</span><span class="sxs-lookup"><span data-stu-id="71076-147">System.String</span></span>

### <span data-ttu-id="71076-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="71076-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="71076-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71076-149">OUTPUTS</span></span>

### <span data-ttu-id="71076-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="71076-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="71076-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="71076-151">NOTES</span></span>

## <span data-ttu-id="71076-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71076-152">RELATED LINKS</span></span>

[<span data-ttu-id="71076-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="71076-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="71076-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="71076-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="71076-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="71076-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
