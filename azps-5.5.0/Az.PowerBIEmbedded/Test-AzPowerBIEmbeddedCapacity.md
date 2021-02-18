---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193103"
---
# <span data-ttu-id="fe3cc-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fe3cc-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fe3cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3cc-103">Verifica la presenza di un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="fe3cc-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fe3cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe3cc-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3cc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fe3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="fe3cc-106">Il cmdlet Test-AzPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="fe3cc-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="fe3cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe3cc-107">EXAMPLES</span></span>

### <span data-ttu-id="fe3cc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe3cc-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="fe3cc-109">Questo comando verifica se esiste una capacità denominata testcapacity</span><span class="sxs-lookup"><span data-stu-id="fe3cc-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="fe3cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3cc-110">PARAMETERS</span></span>

### <span data-ttu-id="fe3cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3cc-111">-DefaultProfile</span></span>
<span data-ttu-id="fe3cc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3cc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fe3cc-113">-Name</span></span>
<span data-ttu-id="fe3cc-114">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="fe3cc-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="fe3cc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3cc-115">CommonParameters</span></span>
<span data-ttu-id="fe3cc-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3cc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3cc-117">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3cc-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3cc-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="fe3cc-118">INPUTS</span></span>

### <span data-ttu-id="fe3cc-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fe3cc-119">None</span></span>

## <span data-ttu-id="fe3cc-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe3cc-120">OUTPUTS</span></span>

### <span data-ttu-id="fe3cc-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe3cc-121">System.Boolean</span></span>

## <span data-ttu-id="fe3cc-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="fe3cc-122">NOTES</span></span>

## <span data-ttu-id="fe3cc-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe3cc-123">RELATED LINKS</span></span>

[<span data-ttu-id="fe3cc-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fe3cc-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="fe3cc-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fe3cc-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
