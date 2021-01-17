---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474426"
---
# <span data-ttu-id="477a2-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="477a2-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="477a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="477a2-102">SYNOPSIS</span></span>
<span data-ttu-id="477a2-103">Aggiorna/imposta un set di record in una zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="477a2-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="477a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="477a2-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="477a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="477a2-105">DESCRIPTION</span></span>
<span data-ttu-id="477a2-106">Il cmdlet Set-AzPrivateDnsRecordSet aggiorna un set di record nel servizio DNS privato di Azure da un oggetto RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="477a2-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="477a2-107">Puoi passare un oggetto RecordSet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="477a2-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="477a2-108">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="477a2-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="477a2-109">Il set di record non viene aggiornato se è stato modificato in Azure private DNS dopo che è stato recuperato l'oggetto RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="477a2-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="477a2-110">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="477a2-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="477a2-111">Puoi eliminare questo comportamento usando il parametro overwrite, che aggiorna il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="477a2-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="477a2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="477a2-112">EXAMPLES</span></span>

### <span data-ttu-id="477a2-113">Esempio 1: aggiornare un set di record</span><span class="sxs-lookup"><span data-stu-id="477a2-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="477a2-114">Il primo comando usa il cmdlet Get-AzPrivateDnsRecordSet per ottenere il set di record specificato e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="477a2-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="477a2-115">Il secondo e il terzo comando sono operazioni off-line per aggiungere due record al set di record.</span><span class="sxs-lookup"><span data-stu-id="477a2-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="477a2-116">Il comando finale usa il cmdlet Set-AzPrivateDnsRecordSet per eseguire il commit dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="477a2-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="477a2-117">Esempio 2: aggiornare un record SOA</span><span class="sxs-lookup"><span data-stu-id="477a2-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="477a2-118">Il primo comando usa il cmdlet Get-AzPrivateDnsRecordSet per ottenere il set di record specificato e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="477a2-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="477a2-119">Il secondo comando Aggiorna il record SOA specificato in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="477a2-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="477a2-120">Il comando finale usa il cmdlet Set-AzPrivateDnsRecordSet per propagare l'aggiornamento in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="477a2-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="477a2-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="477a2-121">PARAMETERS</span></span>

### <span data-ttu-id="477a2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477a2-122">-DefaultProfile</span></span>
<span data-ttu-id="477a2-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="477a2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="477a2-124">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="477a2-124">-Overwrite</span></span>
<span data-ttu-id="477a2-125">Non usare il campo ETag del parametro RecordSet per i controlli di concorrenza ottimistica.</span><span class="sxs-lookup"><span data-stu-id="477a2-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="477a2-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="477a2-126">-RecordSet</span></span>
<span data-ttu-id="477a2-127">Set di record in cui aggiungere il record.</span><span class="sxs-lookup"><span data-stu-id="477a2-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="477a2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="477a2-128">-Confirm</span></span>
<span data-ttu-id="477a2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="477a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="477a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="477a2-130">-WhatIf</span></span>
<span data-ttu-id="477a2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="477a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="477a2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="477a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="477a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477a2-133">CommonParameters</span></span>
<span data-ttu-id="477a2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477a2-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477a2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477a2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="477a2-136">INPUTS</span></span>

### <span data-ttu-id="477a2-137">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="477a2-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="477a2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="477a2-138">OUTPUTS</span></span>

### <span data-ttu-id="477a2-139">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="477a2-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="477a2-140">Note</span><span class="sxs-lookup"><span data-stu-id="477a2-140">NOTES</span></span>

## <span data-ttu-id="477a2-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="477a2-141">RELATED LINKS</span></span>
