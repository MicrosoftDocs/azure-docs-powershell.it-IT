---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186631"
---
# <span data-ttu-id="3bc89-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3bc89-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="3bc89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc89-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc89-103">Elimina un set di record da un'area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="3bc89-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="3bc89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bc89-104">SYNTAX</span></span>

### <span data-ttu-id="3bc89-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bc89-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc89-106">Misto</span><span class="sxs-lookup"><span data-stu-id="3bc89-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc89-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="3bc89-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc89-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc89-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc89-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3bc89-109">DESCRIPTION</span></span>
<span data-ttu-id="3bc89-110">Il Remove-AzPrivateDnsRecordSet cmdlet elimina il set di record specificato dall'area specificata.</span><span class="sxs-lookup"><span data-stu-id="3bc89-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="3bc89-111">Non è possibile eliminare i record SOA creati automaticamente nell'apice dell'area privata.</span><span class="sxs-lookup"><span data-stu-id="3bc89-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="3bc89-112">È possibile passare un oggetto RecordSet a questo cmdlet usando l'operatore della pipeline oppure come parametro o come ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3bc89-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="3bc89-113">Per identificare un record in base al nome e al tipo senza usare un oggetto RecordSet, è necessario passare l'area come oggetto PSPrivateDnsZone a questo cmdlet usando l'operatore della pipeline o come parametro oppure è possibile specificare i parametri ZoneName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3bc89-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="3bc89-114">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="3bc89-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="3bc89-115">Quando si specifica il set di record con un oggetto RecordSet, il set di record non viene eliminato se è stato modificato nel DNS privato di Azure dopo il recupero dell'oggetto RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="3bc89-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="3bc89-116">Questo fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="3bc89-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="3bc89-117">È possibile eliminare questa operazione usando il parametro Overwrite, che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="3bc89-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="3bc89-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bc89-118">EXAMPLES</span></span>

### <span data-ttu-id="3bc89-119">Esempio 1: Rimuovere un set di record</span><span class="sxs-lookup"><span data-stu-id="3bc89-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="3bc89-120">Il primo comando ottiene il set di record specificato e quindi lo archivia nella $RecordSet variabile. Il secondo comando rimuove il set di record in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3bc89-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="3bc89-121">Esempio 2: Rimuovere un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="3bc89-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="3bc89-122">Il primo comando ottiene il set di record specificato.</span><span class="sxs-lookup"><span data-stu-id="3bc89-122">The first command gets the specified record set.</span></span> <span data-ttu-id="3bc89-123">Il secondo comando elimina il set di record, anche se è stato modificato nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="3bc89-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="3bc89-124">Le richieste di conferma vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="3bc89-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="3bc89-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bc89-125">PARAMETERS</span></span>

### <span data-ttu-id="3bc89-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc89-126">-DefaultProfile</span></span>
<span data-ttu-id="3bc89-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc89-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc89-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3bc89-128">-Name</span></span>
<span data-ttu-id="3bc89-129">Nome dei record nel set di record(relativo al nome dell'area e senza punto di chiusura).</span><span class="sxs-lookup"><span data-stu-id="3bc89-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="3bc89-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3bc89-130">-Overwrite</span></span>
<span data-ttu-id="3bc89-131">Non usare il campo ETag del parametro RecordSet per i controlli di concorrenza ottimistica.</span><span class="sxs-lookup"><span data-stu-id="3bc89-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="3bc89-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bc89-132">-PassThru</span></span>
<span data-ttu-id="3bc89-133">Consente di passare il risultato (booleano) dell'operazione di eliminazione dell'area privata più in basso nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="3bc89-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="3bc89-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="3bc89-134">-RecordSet</span></span>
<span data-ttu-id="3bc89-135">Set di record in cui aggiungere il record.</span><span class="sxs-lookup"><span data-stu-id="3bc89-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="3bc89-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="3bc89-136">-RecordType</span></span>
<span data-ttu-id="3bc89-137">Tipo di record DNS privati nel set di record.</span><span class="sxs-lookup"><span data-stu-id="3bc89-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="3bc89-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc89-138">-ResourceGroupName</span></span>
<span data-ttu-id="3bc89-139">Gruppo di risorse a cui appartiene l'area.</span><span class="sxs-lookup"><span data-stu-id="3bc89-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="3bc89-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc89-140">-ResourceId</span></span>
<span data-ttu-id="3bc89-141">ID risorsa RecordSet DNS privato.</span><span class="sxs-lookup"><span data-stu-id="3bc89-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="3bc89-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="3bc89-142">-Zone</span></span>
<span data-ttu-id="3bc89-143">Oggetto PrivateDnsZone che rappresenta l'area in cui creare il set di record.</span><span class="sxs-lookup"><span data-stu-id="3bc89-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="3bc89-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3bc89-144">-ZoneName</span></span>
<span data-ttu-id="3bc89-145">Area in cui è presente il set di record, senza punto di terminazione.</span><span class="sxs-lookup"><span data-stu-id="3bc89-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="3bc89-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bc89-146">-Confirm</span></span>
<span data-ttu-id="3bc89-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc89-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc89-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc89-148">-WhatIf</span></span>
<span data-ttu-id="3bc89-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bc89-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc89-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bc89-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc89-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc89-151">CommonParameters</span></span>
<span data-ttu-id="3bc89-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc89-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc89-153">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc89-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc89-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="3bc89-154">INPUTS</span></span>

### <span data-ttu-id="3bc89-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="3bc89-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="3bc89-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3bc89-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="3bc89-157">System.String</span><span class="sxs-lookup"><span data-stu-id="3bc89-157">System.String</span></span>

## <span data-ttu-id="3bc89-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bc89-158">OUTPUTS</span></span>

### <span data-ttu-id="3bc89-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3bc89-159">System.Boolean</span></span>

## <span data-ttu-id="3bc89-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="3bc89-160">NOTES</span></span>

## <span data-ttu-id="3bc89-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bc89-161">RELATED LINKS</span></span>
