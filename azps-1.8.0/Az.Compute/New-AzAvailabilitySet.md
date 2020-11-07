---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: c34bbb3cfd753c48a961373a44dd1e9bb4302208
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684784"
---
# <span data-ttu-id="f13d3-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f13d3-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="f13d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f13d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f13d3-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="f13d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f13d3-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f13d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f13d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f13d3-106">Il cmdlet **New-AzAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="f13d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f13d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f13d3-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="f13d3-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="f13d3-109">Questo comando crea un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f13d3-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f13d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f13d3-110">PARAMETERS</span></span>

### <span data-ttu-id="f13d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f13d3-111">-AsJob</span></span>
<span data-ttu-id="f13d3-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f13d3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f13d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13d3-113">-DefaultProfile</span></span>
<span data-ttu-id="f13d3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f13d3-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f13d3-115">-Location</span></span>
<span data-ttu-id="f13d3-116">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f13d3-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="f13d3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f13d3-117">-Name</span></span>
<span data-ttu-id="f13d3-118">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f13d3-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="f13d3-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="f13d3-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="f13d3-120">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f13d3-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="f13d3-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="f13d3-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="f13d3-122">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f13d3-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="f13d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f13d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f13d3-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f13d3-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f13d3-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="f13d3-125">-Sku</span></span>
<span data-ttu-id="f13d3-126">Nome di SKU.</span><span class="sxs-lookup"><span data-stu-id="f13d3-126">The Name of Sku.</span></span>
<span data-ttu-id="f13d3-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13d3-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f13d3-128">Allineato: per i dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="f13d3-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="f13d3-129">Classica: per i dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="f13d3-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="f13d3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f13d3-130">-Tag</span></span>
<span data-ttu-id="f13d3-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f13d3-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="f13d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13d3-132">CommonParameters</span></span>
<span data-ttu-id="f13d3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13d3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f13d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13d3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f13d3-135">INPUTS</span></span>

### <span data-ttu-id="f13d3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f13d3-136">System.String</span></span>

### <span data-ttu-id="f13d3-137">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f13d3-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f13d3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f13d3-138">OUTPUTS</span></span>

### <span data-ttu-id="f13d3-139">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f13d3-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f13d3-140">Note</span><span class="sxs-lookup"><span data-stu-id="f13d3-140">NOTES</span></span>

## <span data-ttu-id="f13d3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f13d3-141">RELATED LINKS</span></span>

[<span data-ttu-id="f13d3-142">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f13d3-142">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f13d3-143">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f13d3-143">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


