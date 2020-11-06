---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521976"
---
# <span data-ttu-id="eef77-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eef77-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="eef77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eef77-102">SYNOPSIS</span></span>
<span data-ttu-id="eef77-103">Crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="eef77-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eef77-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eef77-105">DESCRIPTION</span></span>
<span data-ttu-id="eef77-106">Il cmdlet **New-AzureRmAvailabilitySet** crea un set di disponibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="eef77-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="eef77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eef77-107">EXAMPLES</span></span>

### <span data-ttu-id="eef77-108">Esempio 1: creare un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="eef77-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="eef77-109">Questo comando crea un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="eef77-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="eef77-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eef77-110">PARAMETERS</span></span>

### <span data-ttu-id="eef77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef77-111">-DefaultProfile</span></span>
<span data-ttu-id="eef77-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eef77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef77-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="eef77-113">-Location</span></span>
<span data-ttu-id="eef77-114">Specifica la posizione per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="eef77-114">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="eef77-115">-Managed</span><span class="sxs-lookup"><span data-stu-id="eef77-115">-Managed</span></span>
<span data-ttu-id="eef77-116">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="eef77-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef77-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="eef77-117">-Name</span></span>
<span data-ttu-id="eef77-118">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="eef77-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="eef77-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="eef77-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="eef77-120">Specifica il conteggio dei domini di errore della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="eef77-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="eef77-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="eef77-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="eef77-122">Specifica il conteggio dei domini di aggiornamento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="eef77-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="eef77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef77-123">-ResourceGroupName</span></span>
<span data-ttu-id="eef77-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eef77-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eef77-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="eef77-125">-Sku</span></span>
<span data-ttu-id="eef77-126">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="eef77-126">The Name of Sku</span></span>
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

### <span data-ttu-id="eef77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef77-127">CommonParameters</span></span>
<span data-ttu-id="eef77-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef77-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef77-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef77-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eef77-130">INPUTS</span></span>

## <span data-ttu-id="eef77-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eef77-131">OUTPUTS</span></span>

## <span data-ttu-id="eef77-132">Note</span><span class="sxs-lookup"><span data-stu-id="eef77-132">NOTES</span></span>

## <span data-ttu-id="eef77-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eef77-133">RELATED LINKS</span></span>

[<span data-ttu-id="eef77-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eef77-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="eef77-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eef77-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


