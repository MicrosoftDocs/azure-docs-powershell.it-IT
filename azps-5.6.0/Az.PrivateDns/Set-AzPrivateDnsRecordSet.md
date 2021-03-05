---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 68e55ae6a0c563ecc72e74fc127360ddb35f73f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986689"
---
# <span data-ttu-id="8eaaa-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaaa-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8eaaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaaa-103">Aggiorna/imposta un set di record in un'area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="8eaaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8eaaa-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eaaa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8eaaa-105">DESCRIPTION</span></span>
<span data-ttu-id="8eaaa-106">Il Set-AzPrivateDnsRecordSet cmdlet aggiorna un set di record nel servizio DNS privato di Azure da un oggetto RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="8eaaa-107">È possibile passare un oggetto RecordSet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="8eaaa-108">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="8eaaa-109">Il set di record non viene aggiornato se è stato modificato nel DNS privato di Azure dopo il recupero dell'oggetto RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="8eaaa-110">Questo fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="8eaaa-111">È possibile disattivare questo comportamento usando il parametro Overwrite, che aggiorna il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="8eaaa-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8eaaa-112">EXAMPLES</span></span>

### <span data-ttu-id="8eaaa-113">Esempio 1: Aggiornare un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaaa-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="8eaaa-114">Il primo comando usa il cmdlet Get-AzPrivateDnsRecordSet per ottenere il set di record specificato e quindi lo archivia nella $RecordSet variabile.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="8eaaa-115">Il secondo e il terzo comando sono operazioni non in linea per aggiungere due record A al set di record.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="8eaaa-116">Il comando finale usa il cmdlet Set-AzPrivateDnsRecordSet per eseguire il commit dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="8eaaa-117">Esempio 2: Aggiornare un record SOA</span><span class="sxs-lookup"><span data-stu-id="8eaaa-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="8eaaa-118">Il primo comando usa il cmdlet Get-AzPrivateDnsRecordSet per ottenere il set di record specificato e quindi lo archivia nella $RecordSet variabile.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="8eaaa-119">Il secondo comando aggiorna il record SOA specificato in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="8eaaa-120">Il comando finale usa il cmdlet Set-AzPrivateDnsRecordSet per propagare l'aggiornamento in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="8eaaa-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eaaa-121">PARAMETERS</span></span>

### <span data-ttu-id="8eaaa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eaaa-122">-DefaultProfile</span></span>
<span data-ttu-id="8eaaa-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eaaa-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8eaaa-124">-Overwrite</span></span>
<span data-ttu-id="8eaaa-125">Non usare il campo ETag del parametro RecordSet per i controlli di concorrenza ottimistica.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="8eaaa-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaaa-126">-RecordSet</span></span>
<span data-ttu-id="8eaaa-127">Set di record in cui aggiungere il record.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="8eaaa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8eaaa-128">-Confirm</span></span>
<span data-ttu-id="8eaaa-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eaaa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eaaa-130">-WhatIf</span></span>
<span data-ttu-id="8eaaa-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eaaa-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eaaa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaaa-133">CommonParameters</span></span>
<span data-ttu-id="8eaaa-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaaa-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eaaa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaaa-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="8eaaa-136">INPUTS</span></span>

### <span data-ttu-id="8eaaa-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaaa-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8eaaa-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8eaaa-138">OUTPUTS</span></span>

### <span data-ttu-id="8eaaa-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaaa-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8eaaa-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="8eaaa-140">NOTES</span></span>

## <span data-ttu-id="8eaaa-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8eaaa-141">RELATED LINKS</span></span>
