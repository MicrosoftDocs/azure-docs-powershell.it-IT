---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192267"
---
# <span data-ttu-id="2dfa8-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2dfa8-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="2dfa8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dfa8-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfa8-103">Modificare o modificare un sito Virtual Appliance connesso a una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="2dfa8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dfa8-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dfa8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dfa8-105">DESCRIPTION</span></span>
<span data-ttu-id="2dfa8-106">Il comando Update-AzVirtualApplianceSite modifica una risorsa sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="2dfa8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dfa8-107">EXAMPLES</span></span>

### <span data-ttu-id="2dfa8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2dfa8-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="2dfa8-109">Modificare il prefisso dell'indirizzo per una risorsa sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="2dfa8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dfa8-110">PARAMETERS</span></span>

### <span data-ttu-id="2dfa8-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="2dfa8-111">-AddresssPrefix</span></span>
<span data-ttu-id="2dfa8-112">Prefisso dell'indirizzo per il sito.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfa8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dfa8-113">-AsJob</span></span>
<span data-ttu-id="2dfa8-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2dfa8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dfa8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfa8-115">-DefaultProfile</span></span>
<span data-ttu-id="2dfa8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dfa8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2dfa8-117">-Force</span></span>
<span data-ttu-id="2dfa8-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="2dfa8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2dfa8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dfa8-119">-Name</span></span>
<span data-ttu-id="2dfa8-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfa8-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="2dfa8-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="2dfa8-122">Appliance virtuale di rete a cui è associato il sito.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="2dfa8-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="2dfa8-123">-O365Policy</span></span>
<span data-ttu-id="2dfa8-124">Criteri di breakout di Office 365.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfa8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dfa8-125">-ResourceGroupName</span></span>
<span data-ttu-id="2dfa8-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-126">The resource group name.</span></span>

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

### <span data-ttu-id="2dfa8-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="2dfa8-127">-Tag</span></span>
<span data-ttu-id="2dfa8-128">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfa8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2dfa8-129">-Confirm</span></span>
<span data-ttu-id="2dfa8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dfa8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dfa8-131">-WhatIf</span></span>
<span data-ttu-id="2dfa8-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dfa8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dfa8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfa8-134">CommonParameters</span></span>
<span data-ttu-id="2dfa8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dfa8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfa8-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dfa8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfa8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dfa8-137">INPUTS</span></span>

### <span data-ttu-id="2dfa8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2dfa8-138">System.String</span></span>

### <span data-ttu-id="2dfa8-139">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="2dfa8-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="2dfa8-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2dfa8-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2dfa8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dfa8-141">OUTPUTS</span></span>

### <span data-ttu-id="2dfa8-142">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2dfa8-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="2dfa8-143">Note</span><span class="sxs-lookup"><span data-stu-id="2dfa8-143">NOTES</span></span>

## <span data-ttu-id="2dfa8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dfa8-144">RELATED LINKS</span></span>
