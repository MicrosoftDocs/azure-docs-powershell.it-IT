---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311467"
---
# <span data-ttu-id="9b8e8-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="9b8e8-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="9b8e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8e8-103">Creare un sito connesso a una appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="9b8e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b8e8-104">SYNTAX</span></span>

### <span data-ttu-id="9b8e8-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b8e8-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b8e8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b8e8-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b8e8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b8e8-107">DESCRIPTION</span></span>
<span data-ttu-id="9b8e8-108">Il comando New-AzVirtualApplianceSite crea un sito Virtual Appliance connesso a una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="9b8e8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b8e8-109">EXAMPLES</span></span>

### <span data-ttu-id="9b8e8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b8e8-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="9b8e8-111">Creare un nuovo sito appliance virtuale nel gruppo risorse: testrg.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="9b8e8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b8e8-112">PARAMETERS</span></span>

### <span data-ttu-id="9b8e8-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9b8e8-113">-AddressPrefix</span></span>
<span data-ttu-id="9b8e8-114">Prefisso dell'indirizzo per il sito.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="9b8e8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b8e8-115">-AsJob</span></span>
<span data-ttu-id="9b8e8-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b8e8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b8e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8e8-117">-DefaultProfile</span></span>
<span data-ttu-id="9b8e8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b8e8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9b8e8-119">-Force</span></span>
<span data-ttu-id="9b8e8-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="9b8e8-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9b8e8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b8e8-121">-Name</span></span>
<span data-ttu-id="9b8e8-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e8-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="9b8e8-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="9b8e8-124">L'appliance virtuale di rete a cui è associato il sito.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="9b8e8-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="9b8e8-125">-O365Policy</span></span>
<span data-ttu-id="9b8e8-126">Criteri di breakout di Office 365.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b8e8-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b8e8-129">-ResourceId</span></span>
<span data-ttu-id="9b8e8-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e8-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b8e8-131">-Tag</span></span>
<span data-ttu-id="9b8e8-132">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9b8e8-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b8e8-133">-Confirm</span></span>
<span data-ttu-id="9b8e8-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8e8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8e8-135">-WhatIf</span></span>
<span data-ttu-id="9b8e8-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8e8-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8e8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8e8-138">CommonParameters</span></span>
<span data-ttu-id="9b8e8-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8e8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8e8-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b8e8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8e8-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b8e8-141">INPUTS</span></span>

### <span data-ttu-id="9b8e8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9b8e8-142">System.String</span></span>

### <span data-ttu-id="9b8e8-143">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="9b8e8-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="9b8e8-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b8e8-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b8e8-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b8e8-145">OUTPUTS</span></span>

### <span data-ttu-id="9b8e8-146">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="9b8e8-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="9b8e8-147">Note</span><span class="sxs-lookup"><span data-stu-id="9b8e8-147">NOTES</span></span>

## <span data-ttu-id="9b8e8-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b8e8-148">RELATED LINKS</span></span>
