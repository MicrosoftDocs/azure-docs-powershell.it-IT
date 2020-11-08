---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021040"
---
# <span data-ttu-id="0c63a-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c63a-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="0c63a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c63a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c63a-103">Crea una nuova zona privata DNS.</span><span class="sxs-lookup"><span data-stu-id="0c63a-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="0c63a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c63a-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c63a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c63a-105">DESCRIPTION</span></span>
<span data-ttu-id="0c63a-106">Il cmdlet **New-AzPrivateDnsZone** crea una nuova area DNS (private Domain Name System) nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="0c63a-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="0c63a-107">Devi specificare un nome di zona DNS privato univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="0c63a-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="0c63a-108">Dopo aver creato la zona, usare il cmdlet New-AzPrivateDnsRecordSet per creare set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="0c63a-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="0c63a-109">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="0c63a-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0c63a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c63a-110">EXAMPLES</span></span>

### <span data-ttu-id="0c63a-111">Esempio 1: creare una zona DNS privata</span><span class="sxs-lookup"><span data-stu-id="0c63a-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="0c63a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c63a-112">PARAMETERS</span></span>

### <span data-ttu-id="0c63a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c63a-113">-DefaultProfile</span></span>
<span data-ttu-id="0c63a-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c63a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c63a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c63a-115">-Name</span></span>
<span data-ttu-id="0c63a-116">Specifica il nome dell'area DNS privata da creare.</span><span class="sxs-lookup"><span data-stu-id="0c63a-116">Specifies the name of the private DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c63a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c63a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c63a-118">Specifica il gruppo di risorse in cui creare la zona.</span><span class="sxs-lookup"><span data-stu-id="0c63a-118">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c63a-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c63a-119">-Tag</span></span>
<span data-ttu-id="0c63a-120">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0c63a-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0c63a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c63a-121">-Confirm</span></span>
<span data-ttu-id="0c63a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c63a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c63a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c63a-123">-WhatIf</span></span>
<span data-ttu-id="0c63a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c63a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c63a-125">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c63a-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c63a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c63a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c63a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c63a-127">CommonParameters</span></span>
<span data-ttu-id="0c63a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c63a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c63a-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c63a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c63a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c63a-130">INPUTS</span></span>

### <span data-ttu-id="0c63a-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c63a-131">None</span></span>

## <span data-ttu-id="0c63a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c63a-132">OUTPUTS</span></span>

### <span data-ttu-id="0c63a-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c63a-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="0c63a-134">Note</span><span class="sxs-lookup"><span data-stu-id="0c63a-134">NOTES</span></span>

## <span data-ttu-id="0c63a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c63a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c63a-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c63a-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="0c63a-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0c63a-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="0c63a-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c63a-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
