---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863150"
---
# <span data-ttu-id="dc4c9-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc4c9-101">New-AzDnsZone</span></span>

## <span data-ttu-id="dc4c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc4c9-103">Crea una nuova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="dc4c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc4c9-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc4c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc4c9-106">Il cmdlet **New-AzDnsZone** crea una nuova area DNS (Domain Name System) nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="dc4c9-107">Devi specificare un nome di zona DNS univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="dc4c9-108">Dopo aver creato la zona, usare il cmdlet New-AzDnsRecordSet per creare set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="dc4c9-109">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="dc4c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc4c9-110">EXAMPLES</span></span>

### <span data-ttu-id="dc4c9-111">Esempio 1: creare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="dc4c9-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="dc4c9-112">Questo comando crea una nuova zona DNS denominata myzone.com nel gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="dc4c9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc4c9-113">PARAMETERS</span></span>

### <span data-ttu-id="dc4c9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc4c9-114">-Name</span></span>
<span data-ttu-id="dc4c9-115">Specifica il nome della zona DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc4c9-116">-ResourceGroupName</span></span>
<span data-ttu-id="dc4c9-117">Specifica il gruppo di risorse in cui creare la zona.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c9-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc4c9-118">-Tag</span></span>
<span data-ttu-id="dc4c9-119">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dc4c9-120">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="dc4c9-120">For example:</span></span>

<span data-ttu-id="dc4c9-121">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dc4c9-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c9-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc4c9-122">-Confirm</span></span>
<span data-ttu-id="dc4c9-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc4c9-124">-WhatIf</span></span>
<span data-ttu-id="dc4c9-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc4c9-126">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc4c9-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc4c9-128">CommonParameters</span></span>
<span data-ttu-id="dc4c9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc4c9-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc4c9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc4c9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc4c9-131">INPUTS</span></span>

### <span data-ttu-id="dc4c9-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dc4c9-132">None</span></span>

<span data-ttu-id="dc4c9-133">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="dc4c9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc4c9-134">OUTPUTS</span></span>

### <span data-ttu-id="dc4c9-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="dc4c9-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="dc4c9-136">Questo cmdlet restituisce un oggetto Microsoft. Azure. Commands. DNS. DnsZone che rappresenta la nuova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="dc4c9-137">Note</span><span class="sxs-lookup"><span data-stu-id="dc4c9-137">NOTES</span></span>
<span data-ttu-id="dc4c9-138">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="dc4c9-139">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="dc4c9-140">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="dc4c9-141">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dc4c9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc4c9-142">RELATED LINKS</span></span>

[<span data-ttu-id="dc4c9-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc4c9-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="dc4c9-144">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dc4c9-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="dc4c9-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc4c9-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)