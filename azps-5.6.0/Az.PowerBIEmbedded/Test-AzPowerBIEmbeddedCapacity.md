---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996084"
---
# <span data-ttu-id="029f5-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="029f5-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="029f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="029f5-102">SYNOPSIS</span></span>
<span data-ttu-id="029f5-103">Verifica la presenza di un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="029f5-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="029f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="029f5-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="029f5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="029f5-105">DESCRIPTION</span></span>
<span data-ttu-id="029f5-106">Il cmdlet Test-AzPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="029f5-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="029f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="029f5-107">EXAMPLES</span></span>

### <span data-ttu-id="029f5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="029f5-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="029f5-109">Questo comando verifica se esiste una capacità denominata testcapacity</span><span class="sxs-lookup"><span data-stu-id="029f5-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="029f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="029f5-110">PARAMETERS</span></span>

### <span data-ttu-id="029f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029f5-111">-DefaultProfile</span></span>
<span data-ttu-id="029f5-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="029f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="029f5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="029f5-113">-Name</span></span>
<span data-ttu-id="029f5-114">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="029f5-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="029f5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029f5-115">CommonParameters</span></span>
<span data-ttu-id="029f5-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="029f5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029f5-117">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="029f5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029f5-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="029f5-118">INPUTS</span></span>

### <span data-ttu-id="029f5-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="029f5-119">None</span></span>

## <span data-ttu-id="029f5-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="029f5-120">OUTPUTS</span></span>

### <span data-ttu-id="029f5-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="029f5-121">System.Boolean</span></span>

## <span data-ttu-id="029f5-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="029f5-122">NOTES</span></span>

## <span data-ttu-id="029f5-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="029f5-123">RELATED LINKS</span></span>

[<span data-ttu-id="029f5-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="029f5-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="029f5-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="029f5-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
