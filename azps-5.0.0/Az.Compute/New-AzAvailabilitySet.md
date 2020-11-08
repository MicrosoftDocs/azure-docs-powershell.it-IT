---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200254"
---
# <span data-ttu-id="42e07-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42e07-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="42e07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42e07-102">SYNOPSIS</span></span>
<span data-ttu-id="42e07-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="42e07-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="42e07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42e07-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42e07-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42e07-105">DESCRIPTION</span></span>
<span data-ttu-id="42e07-106">Il cmdlet **New-AzAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="42e07-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="42e07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42e07-107">EXAMPLES</span></span>

### <span data-ttu-id="42e07-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="42e07-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="42e07-109">Questo comando crea un set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="42e07-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="42e07-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42e07-110">PARAMETERS</span></span>

### <span data-ttu-id="42e07-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42e07-111">-AsJob</span></span>
<span data-ttu-id="42e07-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="42e07-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="42e07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e07-113">-DefaultProfile</span></span>
<span data-ttu-id="42e07-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42e07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e07-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="42e07-115">-Location</span></span>
<span data-ttu-id="42e07-116">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="42e07-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e07-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="42e07-117">-Name</span></span>
<span data-ttu-id="42e07-118">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="42e07-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e07-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="42e07-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="42e07-120">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="42e07-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e07-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="42e07-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="42e07-122">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="42e07-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e07-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="42e07-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="42e07-124">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="42e07-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="42e07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e07-125">-ResourceGroupName</span></span>
<span data-ttu-id="42e07-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42e07-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e07-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="42e07-127">-Sku</span></span>
<span data-ttu-id="42e07-128">Nome di SKU.</span><span class="sxs-lookup"><span data-stu-id="42e07-128">The Name of Sku.</span></span>
<span data-ttu-id="42e07-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="42e07-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42e07-130">Allineato: per i dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="42e07-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="42e07-131">Classica: per i dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="42e07-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e07-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="42e07-132">-Tag</span></span>
<span data-ttu-id="42e07-133">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="42e07-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="42e07-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e07-134">CommonParameters</span></span>
<span data-ttu-id="42e07-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e07-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e07-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42e07-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e07-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42e07-137">INPUTS</span></span>

### <span data-ttu-id="42e07-138">System. String</span><span class="sxs-lookup"><span data-stu-id="42e07-138">System.String</span></span>

### <span data-ttu-id="42e07-139">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42e07-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="42e07-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42e07-140">OUTPUTS</span></span>

### <span data-ttu-id="42e07-141">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42e07-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="42e07-142">Note</span><span class="sxs-lookup"><span data-stu-id="42e07-142">NOTES</span></span>

## <span data-ttu-id="42e07-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42e07-143">RELATED LINKS</span></span>

[<span data-ttu-id="42e07-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42e07-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="42e07-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42e07-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


