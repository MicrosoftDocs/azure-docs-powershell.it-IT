---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514507"
---
# <span data-ttu-id="90210-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90210-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="90210-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90210-102">SYNOPSIS</span></span>
<span data-ttu-id="90210-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="90210-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90210-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90210-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="90210-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90210-105">DESCRIPTION</span></span>
<span data-ttu-id="90210-106">Il cmdlet **New-AzureRmAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="90210-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="90210-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90210-107">EXAMPLES</span></span>

### <span data-ttu-id="90210-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="90210-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="90210-109">Questo comando crea un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="90210-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="90210-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90210-110">PARAMETERS</span></span>

### <span data-ttu-id="90210-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="90210-111">-Location</span></span>
<span data-ttu-id="90210-112">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="90210-112">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-113">-Managed</span><span class="sxs-lookup"><span data-stu-id="90210-113">-Managed</span></span>
<span data-ttu-id="90210-114">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="90210-114">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="90210-115">-Name</span></span>
<span data-ttu-id="90210-116">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="90210-116">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="90210-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="90210-118">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="90210-118">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="90210-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="90210-120">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="90210-120">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90210-121">-ResourceGroupName</span></span>
<span data-ttu-id="90210-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90210-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="90210-123">-Sku</span></span>
<span data-ttu-id="90210-124">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="90210-124">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90210-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90210-125">CommonParameters</span></span>
<span data-ttu-id="90210-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90210-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90210-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90210-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90210-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90210-128">INPUTS</span></span>

### <span data-ttu-id="90210-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="90210-129">None</span></span>
<span data-ttu-id="90210-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="90210-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90210-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90210-131">OUTPUTS</span></span>

## <span data-ttu-id="90210-132">Note</span><span class="sxs-lookup"><span data-stu-id="90210-132">NOTES</span></span>

## <span data-ttu-id="90210-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90210-133">RELATED LINKS</span></span>

[<span data-ttu-id="90210-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90210-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="90210-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90210-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


