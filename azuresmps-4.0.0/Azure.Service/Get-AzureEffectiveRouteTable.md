---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029815"
---
# <span data-ttu-id="e4207-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4207-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="e4207-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4207-102">SYNOPSIS</span></span>
<span data-ttu-id="e4207-103">Ottiene la route applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4207-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="e4207-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4207-104">SYNTAX</span></span>

### <span data-ttu-id="e4207-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="e4207-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e4207-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="e4207-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4207-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4207-107">DESCRIPTION</span></span>
<span data-ttu-id="e4207-108">Il cmdlet **Get-AzureEffectiveRouteTable** ottiene la route applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4207-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="e4207-109">Questa operazione può richiedere alcuni secondi alla fine.</span><span class="sxs-lookup"><span data-stu-id="e4207-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="e4207-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4207-110">EXAMPLES</span></span>

### <span data-ttu-id="e4207-111">Esempio 1: ottenere la route effettiva applicata una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e4207-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="e4207-112">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="e4207-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="e4207-113">Il cmdlet corrente ottiene la route applicata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4207-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="e4207-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4207-114">PARAMETERS</span></span>

### <span data-ttu-id="e4207-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e4207-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="e4207-116">Specifica il nome della scheda di rete per cui questo cmdlet ottiene Route effettive.</span><span class="sxs-lookup"><span data-stu-id="e4207-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4207-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e4207-117">-Profile</span></span>
<span data-ttu-id="e4207-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4207-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e4207-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e4207-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4207-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="e4207-120">-RoleInstanceName</span></span>
<span data-ttu-id="e4207-121">Specifica il nome di un ruolo PaaS per il quale questo cmdlet ottiene Route effettive.</span><span class="sxs-lookup"><span data-stu-id="e4207-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4207-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4207-122">-ServiceName</span></span>
<span data-ttu-id="e4207-123">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e4207-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="e4207-124">Il ruolo PaaS per cui questo cmdlet ottiene Route effettive appartiene al servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e4207-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4207-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="e4207-125">-Slot</span></span>
<span data-ttu-id="e4207-126">Specifica uno slot PaaS.</span><span class="sxs-lookup"><span data-stu-id="e4207-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="e4207-127">Il ruolo PaaS per cui questo cmdlet ottiene Route effettive include lo slot specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e4207-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="e4207-128">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e4207-128">Valid values are:</span></span> 

- <span data-ttu-id="e4207-129">Produzione</span><span class="sxs-lookup"><span data-stu-id="e4207-129">Production</span></span>
- <span data-ttu-id="e4207-130">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="e4207-130">Staging</span></span> 

<span data-ttu-id="e4207-131">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="e4207-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4207-132">-VM</span><span class="sxs-lookup"><span data-stu-id="e4207-132">-VM</span></span>
<span data-ttu-id="e4207-133">Specifica l'oggetto macchina virtuale per cui questo cmdlet ottiene Route effettive.</span><span class="sxs-lookup"><span data-stu-id="e4207-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4207-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4207-134">CommonParameters</span></span>
<span data-ttu-id="e4207-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4207-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4207-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4207-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4207-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4207-137">INPUTS</span></span>

## <span data-ttu-id="e4207-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4207-138">OUTPUTS</span></span>

### <span data-ttu-id="e4207-139">System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. Models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network></span><span class="sxs-lookup"><span data-stu-id="e4207-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="e4207-140">Note</span><span class="sxs-lookup"><span data-stu-id="e4207-140">NOTES</span></span>

## <span data-ttu-id="e4207-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4207-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4207-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4207-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="e4207-143">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4207-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="e4207-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4207-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="e4207-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4207-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="e4207-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4207-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


