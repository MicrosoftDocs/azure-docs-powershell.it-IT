---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018291"
---
# <span data-ttu-id="16cb6-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="16cb6-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="16cb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="16cb6-103">Verifica l'esistenza di un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="16cb6-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="16cb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16cb6-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16cb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="16cb6-106">Il cmdlet Test-AzPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="16cb6-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="16cb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16cb6-107">EXAMPLES</span></span>

### <span data-ttu-id="16cb6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16cb6-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="16cb6-109">Questo comando testerà se esiste una capacità denominata testcapacity</span><span class="sxs-lookup"><span data-stu-id="16cb6-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="16cb6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16cb6-110">PARAMETERS</span></span>

### <span data-ttu-id="16cb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16cb6-111">-DefaultProfile</span></span>
<span data-ttu-id="16cb6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16cb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16cb6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="16cb6-113">-Name</span></span>
<span data-ttu-id="16cb6-114">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="16cb6-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="16cb6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16cb6-115">CommonParameters</span></span>
<span data-ttu-id="16cb6-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16cb6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16cb6-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16cb6-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16cb6-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16cb6-118">INPUTS</span></span>

### <span data-ttu-id="16cb6-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16cb6-119">None</span></span>

## <span data-ttu-id="16cb6-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16cb6-120">OUTPUTS</span></span>

### <span data-ttu-id="16cb6-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16cb6-121">System.Boolean</span></span>

## <span data-ttu-id="16cb6-122">Note</span><span class="sxs-lookup"><span data-stu-id="16cb6-122">NOTES</span></span>

## <span data-ttu-id="16cb6-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16cb6-123">RELATED LINKS</span></span>

[<span data-ttu-id="16cb6-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="16cb6-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="16cb6-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="16cb6-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
