---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686372"
---
# <span data-ttu-id="d1afa-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1afa-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1afa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1afa-102">SYNOPSIS</span></span>
<span data-ttu-id="d1afa-103">Verifica l'esistenza di un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d1afa-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1afa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1afa-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1afa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1afa-105">DESCRIPTION</span></span>
<span data-ttu-id="d1afa-106">Il cmdlet Test-AzureRmPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="d1afa-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d1afa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1afa-107">EXAMPLES</span></span>

### <span data-ttu-id="d1afa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1afa-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="d1afa-109">Questo comando testerà se esiste una capacità denominata testcapacity</span><span class="sxs-lookup"><span data-stu-id="d1afa-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="d1afa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1afa-110">PARAMETERS</span></span>

### <span data-ttu-id="d1afa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1afa-111">-DefaultProfile</span></span>
<span data-ttu-id="d1afa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1afa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1afa-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1afa-113">-Name</span></span>
<span data-ttu-id="d1afa-114">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="d1afa-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1afa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1afa-115">CommonParameters</span></span>
<span data-ttu-id="d1afa-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1afa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1afa-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1afa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1afa-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1afa-118">INPUTS</span></span>

### <span data-ttu-id="d1afa-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1afa-119">None</span></span>

## <span data-ttu-id="d1afa-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1afa-120">OUTPUTS</span></span>

### <span data-ttu-id="d1afa-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1afa-121">System.Boolean</span></span>

## <span data-ttu-id="d1afa-122">Note</span><span class="sxs-lookup"><span data-stu-id="d1afa-122">NOTES</span></span>

## <span data-ttu-id="d1afa-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1afa-123">RELATED LINKS</span></span>

[<span data-ttu-id="d1afa-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1afa-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d1afa-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1afa-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
