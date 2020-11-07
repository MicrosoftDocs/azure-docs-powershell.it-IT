---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 80fc102c31e4019576a6f2c65ee1c93e19b81590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855917"
---
# <span data-ttu-id="3f1c4-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3f1c4-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3f1c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1c4-103">Verifica l'esistenza di un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3f1c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f1c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f1c4-105">DESCRIPTION</span></span>
<span data-ttu-id="3f1c4-106">Il cmdlet Test-AzPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3f1c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-107">EXAMPLES</span></span>

### <span data-ttu-id="3f1c4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f1c4-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="3f1c4-109">Questo comando testerà se esiste una capacità denominata testcapacity</span><span class="sxs-lookup"><span data-stu-id="3f1c4-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="3f1c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1c4-111">-DefaultProfile</span></span>
<span data-ttu-id="3f1c4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f1c4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f1c4-113">-Name</span></span>
<span data-ttu-id="3f1c4-114">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3f1c4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1c4-115">CommonParameters</span></span>
<span data-ttu-id="3f1c4-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1c4-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1c4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1c4-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-118">INPUTS</span></span>

### <span data-ttu-id="3f1c4-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f1c4-119">None</span></span>

## <span data-ttu-id="3f1c4-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f1c4-120">OUTPUTS</span></span>

### <span data-ttu-id="3f1c4-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f1c4-121">System.Boolean</span></span>

## <span data-ttu-id="3f1c4-122">Note</span><span class="sxs-lookup"><span data-stu-id="3f1c4-122">NOTES</span></span>

## <span data-ttu-id="3f1c4-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f1c4-123">RELATED LINKS</span></span>

[<span data-ttu-id="3f1c4-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3f1c4-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3f1c4-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3f1c4-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
