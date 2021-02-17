---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205859"
---
# <span data-ttu-id="fde0d-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fde0d-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="fde0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde0d-102">SYNOPSIS</span></span>
<span data-ttu-id="fde0d-103">Verifica la presenza di un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fde0d-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="fde0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fde0d-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fde0d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fde0d-105">DESCRIPTION</span></span>
<span data-ttu-id="fde0d-106">Il cmdlet Test-AzAnalysisServicesServer verifica l'esistenza di un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fde0d-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="fde0d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fde0d-107">EXAMPLES</span></span>

### <span data-ttu-id="fde0d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fde0d-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="fde0d-109">Questo comando verifica se nel gruppo di test del gruppo di risorse è presente un server denominato testserver</span><span class="sxs-lookup"><span data-stu-id="fde0d-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="fde0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fde0d-110">PARAMETERS</span></span>

### <span data-ttu-id="fde0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde0d-111">-DefaultProfile</span></span>
<span data-ttu-id="fde0d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fde0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fde0d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fde0d-113">-Name</span></span>
<span data-ttu-id="fde0d-114">Nome del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fde0d-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="fde0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="fde0d-116">Nome del gruppo di risorse di Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="fde0d-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fde0d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde0d-117">CommonParameters</span></span>
<span data-ttu-id="fde0d-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde0d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde0d-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde0d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde0d-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="fde0d-120">INPUTS</span></span>

### <span data-ttu-id="fde0d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fde0d-121">System.String</span></span>

## <span data-ttu-id="fde0d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fde0d-122">OUTPUTS</span></span>

### <span data-ttu-id="fde0d-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fde0d-123">System.Boolean</span></span>

## <span data-ttu-id="fde0d-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="fde0d-124">NOTES</span></span>
<span data-ttu-id="fde0d-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="fde0d-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="fde0d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fde0d-126">RELATED LINKS</span></span>

[<span data-ttu-id="fde0d-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fde0d-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="fde0d-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fde0d-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
