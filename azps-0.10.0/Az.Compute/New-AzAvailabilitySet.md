---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863670"
---
# <span data-ttu-id="85c55-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85c55-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="85c55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85c55-102">SYNOPSIS</span></span>
<span data-ttu-id="85c55-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="85c55-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="85c55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85c55-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85c55-105">DESCRIPTION</span></span>
<span data-ttu-id="85c55-106">Il cmdlet **New-AzAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="85c55-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="85c55-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85c55-107">EXAMPLES</span></span>

### <span data-ttu-id="85c55-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="85c55-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="85c55-109">Questo comando crea un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="85c55-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="85c55-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85c55-110">PARAMETERS</span></span>

### <span data-ttu-id="85c55-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85c55-111">-AsJob</span></span>
<span data-ttu-id="85c55-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="85c55-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="85c55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c55-113">-DefaultProfile</span></span>
<span data-ttu-id="85c55-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85c55-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c55-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="85c55-115">-Location</span></span>
<span data-ttu-id="85c55-116">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="85c55-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="85c55-117">-Managed</span><span class="sxs-lookup"><span data-stu-id="85c55-117">-Managed</span></span>
<span data-ttu-id="85c55-118">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="85c55-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="85c55-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="85c55-119">-Name</span></span>
<span data-ttu-id="85c55-120">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="85c55-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="85c55-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="85c55-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="85c55-122">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="85c55-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="85c55-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="85c55-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="85c55-124">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="85c55-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="85c55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c55-125">-ResourceGroupName</span></span>
<span data-ttu-id="85c55-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85c55-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85c55-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="85c55-127">-Sku</span></span>
<span data-ttu-id="85c55-128">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="85c55-128">The Name of Sku</span></span>
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

### <span data-ttu-id="85c55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c55-129">CommonParameters</span></span>
<span data-ttu-id="85c55-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c55-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c55-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c55-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85c55-132">INPUTS</span></span>

### <span data-ttu-id="85c55-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85c55-133">None</span></span>
<span data-ttu-id="85c55-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="85c55-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85c55-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85c55-135">OUTPUTS</span></span>

### <span data-ttu-id="85c55-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85c55-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="85c55-137">Note</span><span class="sxs-lookup"><span data-stu-id="85c55-137">NOTES</span></span>

## <span data-ttu-id="85c55-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85c55-138">RELATED LINKS</span></span>

[<span data-ttu-id="85c55-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85c55-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="85c55-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85c55-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


