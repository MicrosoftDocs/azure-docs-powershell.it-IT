---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: a5c4ae9492d64bc8c84439f747031d6facd88673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855849"
---
# <span data-ttu-id="546f6-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="546f6-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="546f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="546f6-102">SYNOPSIS</span></span>
<span data-ttu-id="546f6-103">Aggiorna una zona DNS privata da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="546f6-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="546f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="546f6-104">SYNTAX</span></span>

### <span data-ttu-id="546f6-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="546f6-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="546f6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="546f6-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="546f6-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="546f6-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="546f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="546f6-108">DESCRIPTION</span></span>
<span data-ttu-id="546f6-109">Il cmdlet **set-AzPrivateDnsZone** aggiorna in modo permanente una zona DNS (Domain Name System) privata da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="546f6-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="546f6-110">Puoi passare un oggetto **PrivateDnsZone** usando il parametro *PrivateZone* o usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="546f6-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="546f6-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="546f6-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="546f6-112">Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene aggiornata se è stata modificata in Azure DNS, poiché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come modifiche, le operazioni sui set di record all'interno della zona non lo sono).</span><span class="sxs-lookup"><span data-stu-id="546f6-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="546f6-113">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="546f6-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="546f6-114">Questa operazione può essere eliminata usando il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="546f6-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="546f6-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="546f6-115">EXAMPLES</span></span>

### <span data-ttu-id="546f6-116">Esempio 1: aggiorna un'area privata</span><span class="sxs-lookup"><span data-stu-id="546f6-116">Example 1: Updates a private zone</span></span>
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

## <span data-ttu-id="546f6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="546f6-117">PARAMETERS</span></span>

### <span data-ttu-id="546f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546f6-118">-DefaultProfile</span></span>
<span data-ttu-id="546f6-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="546f6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="546f6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="546f6-120">-Name</span></span>
<span data-ttu-id="546f6-121">Specifica il nome dell'area DNS privata che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="546f6-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="546f6-122">Devi anche specificare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="546f6-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="546f6-123">In alternativa, puoi specificare la zona DNS privata usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="546f6-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="546f6-124">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="546f6-124">-Overwrite</span></span>
<span data-ttu-id="546f6-125">Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene aggiornata se è stata modificata in Azure DNS, poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come modifiche, le operazioni sui set di record all'interno della zona non lo sono).</span><span class="sxs-lookup"><span data-stu-id="546f6-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="546f6-126">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="546f6-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="546f6-127">Questa operazione può essere eliminata usando il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="546f6-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="546f6-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="546f6-128">-PrivateZone</span></span>
<span data-ttu-id="546f6-129">Oggetto zone da impostare.</span><span class="sxs-lookup"><span data-stu-id="546f6-129">The zone object to set.</span></span>

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

### <span data-ttu-id="546f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="546f6-131">Specifica il nome del gruppo di risorse che contiene la zona da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="546f6-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="546f6-132">Devi anche specificare il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="546f6-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="546f6-133">In alternativa, puoi specificare la zona DNS privata usando un oggetto **dnsZone** , passato tramite il parametro pipeline o *zone* .</span><span class="sxs-lookup"><span data-stu-id="546f6-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="546f6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="546f6-134">-ResourceId</span></span>
<span data-ttu-id="546f6-135">Area DNS privata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="546f6-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="546f6-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="546f6-136">-Tag</span></span>
<span data-ttu-id="546f6-137">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="546f6-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="546f6-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="546f6-138">-Confirm</span></span>
<span data-ttu-id="546f6-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="546f6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="546f6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546f6-140">-WhatIf</span></span>
<span data-ttu-id="546f6-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="546f6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="546f6-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="546f6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="546f6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546f6-143">CommonParameters</span></span>
<span data-ttu-id="546f6-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546f6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546f6-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546f6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546f6-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="546f6-146">INPUTS</span></span>

### <span data-ttu-id="546f6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="546f6-147">System.String</span></span>

### <span data-ttu-id="546f6-148">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="546f6-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="546f6-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="546f6-149">OUTPUTS</span></span>

### <span data-ttu-id="546f6-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="546f6-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="546f6-151">Note</span><span class="sxs-lookup"><span data-stu-id="546f6-151">NOTES</span></span>

## <span data-ttu-id="546f6-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="546f6-152">RELATED LINKS</span></span>

[<span data-ttu-id="546f6-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="546f6-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="546f6-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="546f6-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="546f6-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="546f6-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
