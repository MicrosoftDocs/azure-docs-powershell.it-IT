---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 0b54ebe9650ba8dcd382afd308b21e7c48d1062d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855874"
---
# <span data-ttu-id="72daa-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72daa-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="72daa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72daa-102">SYNOPSIS</span></span>
<span data-ttu-id="72daa-103">Elimina un set di record da una zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="72daa-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="72daa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72daa-104">SYNTAX</span></span>

### <span data-ttu-id="72daa-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72daa-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72daa-106">Misto</span><span class="sxs-lookup"><span data-stu-id="72daa-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72daa-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="72daa-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72daa-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="72daa-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72daa-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72daa-109">DESCRIPTION</span></span>
<span data-ttu-id="72daa-110">Il cmdlet Remove-AzPrivateDnsRecordSet Elimina il set di record specificato dalla zona specificata.</span><span class="sxs-lookup"><span data-stu-id="72daa-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="72daa-111">Non è possibile eliminare i record SOA creati automaticamente nell'Apex zona privata.</span><span class="sxs-lookup"><span data-stu-id="72daa-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="72daa-112">Puoi passare un oggetto RecordSet a questo cmdlet usando l'operatore pipeline o come parametro o come ResourceId.</span><span class="sxs-lookup"><span data-stu-id="72daa-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="72daa-113">Per identificare un record impostato per nome e tipo senza usare un oggetto RecordSet, devi passare la zona come oggetto PSPrivateDnsZone a questo cmdlet usando l'operatore della pipeline o come parametro oppure puoi specificare i parametri zonename e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="72daa-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="72daa-114">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="72daa-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="72daa-115">Quando specifichi il set di record usando un oggetto RecordSet, il set di record non viene eliminato se è stato modificato in Azure private DNS dopo che è stato recuperato l'oggetto RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="72daa-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="72daa-116">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="72daa-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="72daa-117">Puoi eliminarlo usando il parametro overwrite, che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="72daa-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="72daa-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72daa-118">EXAMPLES</span></span>

### <span data-ttu-id="72daa-119">Esempio 1: rimuovere un set di record</span><span class="sxs-lookup"><span data-stu-id="72daa-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="72daa-120">Il primo comando ottiene il set di record specificato e lo archivia nella variabile $RecordSet. Il secondo comando rimuove il set di record in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="72daa-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="72daa-121">Esempio 2: rimuovere un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="72daa-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="72daa-122">Il primo comando ottiene il set di record specificato.</span><span class="sxs-lookup"><span data-stu-id="72daa-122">The first command gets the specified record set.</span></span> <span data-ttu-id="72daa-123">Il secondo comando Elimina il set di record, anche se è stato modificato nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="72daa-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="72daa-124">Le richieste di conferma vengono soppresse.</span><span class="sxs-lookup"><span data-stu-id="72daa-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="72daa-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72daa-125">PARAMETERS</span></span>

### <span data-ttu-id="72daa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72daa-126">-DefaultProfile</span></span>
<span data-ttu-id="72daa-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72daa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72daa-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="72daa-128">-Name</span></span>
<span data-ttu-id="72daa-129">Nome dei record nel set di record (relativo al nome della zona e senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="72daa-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72daa-130">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="72daa-130">-Overwrite</span></span>
<span data-ttu-id="72daa-131">Non usare il campo ETag del parametro RecordSet per i controlli di concorrenza ottimistica.</span><span class="sxs-lookup"><span data-stu-id="72daa-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="72daa-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72daa-132">-PassThru</span></span>
<span data-ttu-id="72daa-133">Usato per passare il risultato (booleano) dell'operazione elimina l'area privata più avanti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="72daa-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="72daa-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="72daa-134">-RecordSet</span></span>
<span data-ttu-id="72daa-135">Set di record in cui aggiungere il record.</span><span class="sxs-lookup"><span data-stu-id="72daa-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72daa-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="72daa-136">-RecordType</span></span>
<span data-ttu-id="72daa-137">Tipo di record DNS privati nel set di record.</span><span class="sxs-lookup"><span data-stu-id="72daa-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72daa-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72daa-138">-ResourceGroupName</span></span>
<span data-ttu-id="72daa-139">Il gruppo di risorse a cui appartiene la zona.</span><span class="sxs-lookup"><span data-stu-id="72daa-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="72daa-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72daa-140">-ResourceId</span></span>
<span data-ttu-id="72daa-141">ResourceID del RecordSet DNS privato.</span><span class="sxs-lookup"><span data-stu-id="72daa-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="72daa-142">-Zona</span><span class="sxs-lookup"><span data-stu-id="72daa-142">-Zone</span></span>
<span data-ttu-id="72daa-143">Oggetto PrivateDnsZone che rappresenta la zona in cui creare il set di record.</span><span class="sxs-lookup"><span data-stu-id="72daa-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72daa-144">-Zonename</span><span class="sxs-lookup"><span data-stu-id="72daa-144">-ZoneName</span></span>
<span data-ttu-id="72daa-145">Zona in cui è presente il set di record (senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="72daa-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="72daa-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72daa-146">-Confirm</span></span>
<span data-ttu-id="72daa-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72daa-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72daa-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72daa-148">-WhatIf</span></span>
<span data-ttu-id="72daa-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72daa-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72daa-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72daa-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72daa-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72daa-151">CommonParameters</span></span>
<span data-ttu-id="72daa-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72daa-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72daa-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72daa-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72daa-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72daa-154">INPUTS</span></span>

### <span data-ttu-id="72daa-155">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="72daa-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="72daa-156">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72daa-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="72daa-157">System. String</span><span class="sxs-lookup"><span data-stu-id="72daa-157">System.String</span></span>

## <span data-ttu-id="72daa-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72daa-158">OUTPUTS</span></span>

### <span data-ttu-id="72daa-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72daa-159">System.Boolean</span></span>

## <span data-ttu-id="72daa-160">Note</span><span class="sxs-lookup"><span data-stu-id="72daa-160">NOTES</span></span>

## <span data-ttu-id="72daa-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72daa-161">RELATED LINKS</span></span>
