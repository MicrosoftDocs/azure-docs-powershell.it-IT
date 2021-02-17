---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183942"
---
# <span data-ttu-id="37d5d-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="37d5d-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="37d5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="37d5d-103">Crea una nuova area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="37d5d-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="37d5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37d5d-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d5d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="37d5d-106">Il cmdlet **New-AzPrivateDnsZone** crea una nuova area DNS (Domain Name System) privata nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="37d5d-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="37d5d-107">È necessario specificare un nome di zona DNS privato univoco per il parametro *Name,* in modo che il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="37d5d-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="37d5d-108">Dopo aver creato l'area, usare New-AzPrivateDnsRecordSet cmdlet per creare set di record nell'area.</span><span class="sxs-lookup"><span data-stu-id="37d5d-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="37d5d-109">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="37d5d-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="37d5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37d5d-110">EXAMPLES</span></span>

### <span data-ttu-id="37d5d-111">Esempio 1: Creare un'area DNS privata</span><span class="sxs-lookup"><span data-stu-id="37d5d-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="37d5d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37d5d-112">PARAMETERS</span></span>

### <span data-ttu-id="37d5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d5d-113">-DefaultProfile</span></span>
<span data-ttu-id="37d5d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="37d5d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37d5d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="37d5d-115">-Name</span></span>
<span data-ttu-id="37d5d-116">Specifica il nome dell'area DNS privata da creare.</span><span class="sxs-lookup"><span data-stu-id="37d5d-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="37d5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="37d5d-118">Specifica il gruppo di risorse in cui creare l'area.</span><span class="sxs-lookup"><span data-stu-id="37d5d-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="37d5d-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="37d5d-119">-Tag</span></span>
<span data-ttu-id="37d5d-120">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="37d5d-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="37d5d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37d5d-121">-Confirm</span></span>
<span data-ttu-id="37d5d-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37d5d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d5d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d5d-123">-WhatIf</span></span>
<span data-ttu-id="37d5d-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d5d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37d5d-125">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d5d-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37d5d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d5d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d5d-127">CommonParameters</span></span>
<span data-ttu-id="37d5d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d5d-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d5d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d5d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="37d5d-130">INPUTS</span></span>

### <span data-ttu-id="37d5d-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37d5d-131">None</span></span>

## <span data-ttu-id="37d5d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37d5d-132">OUTPUTS</span></span>

### <span data-ttu-id="37d5d-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="37d5d-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="37d5d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="37d5d-134">NOTES</span></span>

## <span data-ttu-id="37d5d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37d5d-135">RELATED LINKS</span></span>

[<span data-ttu-id="37d5d-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="37d5d-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="37d5d-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="37d5d-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="37d5d-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="37d5d-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
