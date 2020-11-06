---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519588"
---
# <span data-ttu-id="65477-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="65477-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="65477-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65477-102">SYNOPSIS</span></span>
<span data-ttu-id="65477-103">Crea una nuova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="65477-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65477-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65477-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65477-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65477-105">DESCRIPTION</span></span>
<span data-ttu-id="65477-106">Il cmdlet **New-AzureRmDnsZone** crea una nuova area DNS (Domain Name System) nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="65477-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="65477-107">Devi specificare un nome di zona DNS univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="65477-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="65477-108">Dopo aver creato la zona, usare il cmdlet New-AzureRmDnsRecordSet per creare set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="65477-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="65477-109">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="65477-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="65477-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65477-110">EXAMPLES</span></span>

### <span data-ttu-id="65477-111">Esempio 1: creare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="65477-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="65477-112">Questo comando crea una nuova zona DNS denominata myzone.com nel gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="65477-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="65477-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65477-113">PARAMETERS</span></span>

### <span data-ttu-id="65477-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="65477-114">-Name</span></span>
<span data-ttu-id="65477-115">Specifica il nome della zona DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="65477-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65477-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65477-116">-ResourceGroupName</span></span>
<span data-ttu-id="65477-117">Specifica il gruppo di risorse in cui creare la zona.</span><span class="sxs-lookup"><span data-stu-id="65477-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65477-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="65477-118">-Tag</span></span>
<span data-ttu-id="65477-119">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="65477-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65477-120">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="65477-120">For example:</span></span>

<span data-ttu-id="65477-121">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="65477-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65477-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65477-122">-Confirm</span></span>
<span data-ttu-id="65477-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65477-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65477-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65477-124">-WhatIf</span></span>
<span data-ttu-id="65477-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65477-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65477-126">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65477-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65477-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65477-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65477-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65477-128">-DefaultProfile</span></span>
<span data-ttu-id="65477-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65477-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65477-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65477-130">CommonParameters</span></span>
<span data-ttu-id="65477-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65477-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65477-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65477-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65477-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65477-133">INPUTS</span></span>

### <span data-ttu-id="65477-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="65477-134">None</span></span>
<span data-ttu-id="65477-135">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65477-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="65477-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65477-136">OUTPUTS</span></span>

### <span data-ttu-id="65477-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="65477-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="65477-138">Questo cmdlet restituisce un oggetto Microsoft. Azure. Commands. DNS. DnsZone che rappresenta la nuova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="65477-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="65477-139">Note</span><span class="sxs-lookup"><span data-stu-id="65477-139">NOTES</span></span>
<span data-ttu-id="65477-140">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="65477-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="65477-141">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="65477-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="65477-142">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="65477-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="65477-143">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="65477-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="65477-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65477-144">RELATED LINKS</span></span>

[<span data-ttu-id="65477-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="65477-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="65477-146">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="65477-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="65477-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="65477-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
