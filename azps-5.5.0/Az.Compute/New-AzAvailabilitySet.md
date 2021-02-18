---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181662"
---
# <span data-ttu-id="f35e9-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f35e9-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="f35e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f35e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f35e9-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="f35e9-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="f35e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f35e9-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f35e9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f35e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f35e9-106">Il cmdlet **New-AzAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="f35e9-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="f35e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f35e9-107">EXAMPLES</span></span>

### <span data-ttu-id="f35e9-108">Esempio 1: Creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="f35e9-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="f35e9-109">Questo comando crea un set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f35e9-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f35e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f35e9-110">PARAMETERS</span></span>

### <span data-ttu-id="f35e9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f35e9-111">-AsJob</span></span>
<span data-ttu-id="f35e9-112">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f35e9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f35e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f35e9-113">-DefaultProfile</span></span>
<span data-ttu-id="f35e9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f35e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f35e9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f35e9-115">-Location</span></span>
<span data-ttu-id="f35e9-116">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f35e9-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="f35e9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f35e9-117">-Name</span></span>
<span data-ttu-id="f35e9-118">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f35e9-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="f35e9-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="f35e9-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="f35e9-120">Specifica il numero di domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f35e9-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="f35e9-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="f35e9-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="f35e9-122">Specifica il numero di domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f35e9-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="f35e9-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="f35e9-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="f35e9-124">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f35e9-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="f35e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f35e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="f35e9-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f35e9-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f35e9-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="f35e9-127">-Sku</span></span>
<span data-ttu-id="f35e9-128">Nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="f35e9-128">The Name of Sku.</span></span>
<span data-ttu-id="f35e9-129">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="f35e9-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f35e9-130">Allineato: per i dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="f35e9-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="f35e9-131">Classico: per i dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="f35e9-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="f35e9-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="f35e9-132">-Tag</span></span>
<span data-ttu-id="f35e9-133">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f35e9-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="f35e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f35e9-134">CommonParameters</span></span>
<span data-ttu-id="f35e9-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f35e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f35e9-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f35e9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f35e9-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="f35e9-137">INPUTS</span></span>

### <span data-ttu-id="f35e9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f35e9-138">System.String</span></span>

### <span data-ttu-id="f35e9-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f35e9-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f35e9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f35e9-140">OUTPUTS</span></span>

### <span data-ttu-id="f35e9-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f35e9-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f35e9-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="f35e9-142">NOTES</span></span>

## <span data-ttu-id="f35e9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f35e9-143">RELATED LINKS</span></span>

[<span data-ttu-id="f35e9-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f35e9-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f35e9-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f35e9-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


