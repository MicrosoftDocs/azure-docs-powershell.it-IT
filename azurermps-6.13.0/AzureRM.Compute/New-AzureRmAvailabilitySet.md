---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687619"
---
# <span data-ttu-id="60d75-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="60d75-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="60d75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60d75-102">SYNOPSIS</span></span>
<span data-ttu-id="60d75-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="60d75-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60d75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60d75-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60d75-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d75-105">DESCRIPTION</span></span>
<span data-ttu-id="60d75-106">Il cmdlet **New-AzureRmAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="60d75-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="60d75-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60d75-107">EXAMPLES</span></span>

### <span data-ttu-id="60d75-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="60d75-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="60d75-109">Questo comando crea un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="60d75-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="60d75-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60d75-110">PARAMETERS</span></span>

### <span data-ttu-id="60d75-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60d75-111">-AsJob</span></span>
<span data-ttu-id="60d75-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="60d75-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="60d75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d75-113">-DefaultProfile</span></span>
<span data-ttu-id="60d75-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60d75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60d75-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="60d75-115">-Location</span></span>
<span data-ttu-id="60d75-116">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="60d75-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="60d75-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="60d75-117">-Name</span></span>
<span data-ttu-id="60d75-118">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="60d75-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="60d75-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="60d75-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="60d75-120">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="60d75-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="60d75-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="60d75-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="60d75-122">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="60d75-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="60d75-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d75-123">-ResourceGroupName</span></span>
<span data-ttu-id="60d75-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60d75-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="60d75-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="60d75-125">-Sku</span></span>
<span data-ttu-id="60d75-126">Nome di SKU.</span><span class="sxs-lookup"><span data-stu-id="60d75-126">The Name of Sku.</span></span>
<span data-ttu-id="60d75-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60d75-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="60d75-128">Allineato: per i dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="60d75-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="60d75-129">Classica: per i dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="60d75-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="60d75-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="60d75-130">-Tag</span></span>
<span data-ttu-id="60d75-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="60d75-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="60d75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d75-132">CommonParameters</span></span>
<span data-ttu-id="60d75-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d75-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d75-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d75-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60d75-135">INPUTS</span></span>

### <span data-ttu-id="60d75-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60d75-136">System.String</span></span>

### <span data-ttu-id="60d75-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="60d75-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="60d75-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60d75-138">OUTPUTS</span></span>

### <span data-ttu-id="60d75-139">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="60d75-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="60d75-140">Note</span><span class="sxs-lookup"><span data-stu-id="60d75-140">NOTES</span></span>

## <span data-ttu-id="60d75-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60d75-141">RELATED LINKS</span></span>

[<span data-ttu-id="60d75-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="60d75-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="60d75-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="60d75-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


