---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865952"
---
# <span data-ttu-id="85fbd-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fbd-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="85fbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="85fbd-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="85fbd-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85fbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85fbd-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85fbd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="85fbd-106">Il cmdlet **New-AzureRmAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="85fbd-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="85fbd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="85fbd-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="85fbd-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="85fbd-109">Questo comando crea un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="85fbd-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="85fbd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="85fbd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85fbd-111">-AsJob</span></span>
<span data-ttu-id="85fbd-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="85fbd-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85fbd-113">-DefaultProfile</span></span>
<span data-ttu-id="85fbd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85fbd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fbd-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="85fbd-115">-Location</span></span>
<span data-ttu-id="85fbd-116">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="85fbd-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="85fbd-117">-Managed</span><span class="sxs-lookup"><span data-stu-id="85fbd-117">-Managed</span></span>
<span data-ttu-id="85fbd-118">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="85fbd-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="85fbd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="85fbd-119">-Name</span></span>
<span data-ttu-id="85fbd-120">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="85fbd-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="85fbd-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="85fbd-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="85fbd-122">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="85fbd-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="85fbd-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="85fbd-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="85fbd-124">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="85fbd-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="85fbd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85fbd-125">-ResourceGroupName</span></span>
<span data-ttu-id="85fbd-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85fbd-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85fbd-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="85fbd-127">-Sku</span></span>
<span data-ttu-id="85fbd-128">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="85fbd-128">The Name of Sku</span></span>
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

### <span data-ttu-id="85fbd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85fbd-129">CommonParameters</span></span>
<span data-ttu-id="85fbd-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85fbd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85fbd-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85fbd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85fbd-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85fbd-132">INPUTS</span></span>

### <span data-ttu-id="85fbd-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85fbd-133">None</span></span>
<span data-ttu-id="85fbd-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="85fbd-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85fbd-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85fbd-135">OUTPUTS</span></span>

### <span data-ttu-id="85fbd-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fbd-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="85fbd-137">Note</span><span class="sxs-lookup"><span data-stu-id="85fbd-137">NOTES</span></span>

## <span data-ttu-id="85fbd-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85fbd-138">RELATED LINKS</span></span>

[<span data-ttu-id="85fbd-139">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fbd-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="85fbd-140">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fbd-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


