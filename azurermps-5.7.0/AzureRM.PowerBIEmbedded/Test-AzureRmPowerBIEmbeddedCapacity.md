---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508083"
---
# <span data-ttu-id="79aa5-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="79aa5-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="79aa5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="79aa5-103">Verifica l'esistenza di un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="79aa5-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79aa5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79aa5-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="79aa5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="79aa5-106">Il cmdlet Test-AzureRmPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="79aa5-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="79aa5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79aa5-107">EXAMPLES</span></span>

### <span data-ttu-id="79aa5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79aa5-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="79aa5-109">Questo comando testerà se esiste una capacità denominata testcapacity</span><span class="sxs-lookup"><span data-stu-id="79aa5-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="79aa5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79aa5-110">PARAMETERS</span></span>

### <span data-ttu-id="79aa5-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="79aa5-111">-Name</span></span>
<span data-ttu-id="79aa5-112">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="79aa5-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="79aa5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79aa5-113">CommonParameters</span></span>
<span data-ttu-id="79aa5-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79aa5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79aa5-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79aa5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79aa5-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79aa5-116">INPUTS</span></span>

### <span data-ttu-id="79aa5-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79aa5-117">None</span></span>
<span data-ttu-id="79aa5-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="79aa5-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79aa5-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79aa5-119">OUTPUTS</span></span>

### <span data-ttu-id="79aa5-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79aa5-120">System.Boolean</span></span>

## <span data-ttu-id="79aa5-121">Note</span><span class="sxs-lookup"><span data-stu-id="79aa5-121">NOTES</span></span>

## <span data-ttu-id="79aa5-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79aa5-122">RELATED LINKS</span></span>

[<span data-ttu-id="79aa5-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="79aa5-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="79aa5-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="79aa5-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
