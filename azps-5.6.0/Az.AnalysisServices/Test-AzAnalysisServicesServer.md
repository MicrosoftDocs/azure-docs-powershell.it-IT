---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: cb6680276359fddcf9a98cde3e90cb44185c4e85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959213"
---
# <span data-ttu-id="8e454-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e454-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="8e454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e454-102">SYNOPSIS</span></span>
<span data-ttu-id="8e454-103">Verifica la presenza di un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e454-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="8e454-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e454-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e454-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e454-105">DESCRIPTION</span></span>
<span data-ttu-id="8e454-106">Il cmdlet Test-AzAnalysisServicesServer verifica l'esistenza di un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e454-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="8e454-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e454-107">EXAMPLES</span></span>

### <span data-ttu-id="8e454-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e454-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="8e454-109">Questo comando verifica se nel gruppo di test del gruppo di risorse è presente un server denominato testserver</span><span class="sxs-lookup"><span data-stu-id="8e454-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="8e454-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e454-110">PARAMETERS</span></span>

### <span data-ttu-id="8e454-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e454-111">-DefaultProfile</span></span>
<span data-ttu-id="8e454-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e454-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e454-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8e454-113">-Name</span></span>
<span data-ttu-id="8e454-114">Nome del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e454-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8e454-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e454-115">-ResourceGroupName</span></span>
<span data-ttu-id="8e454-116">Nome del gruppo di risorse di Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="8e454-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="8e454-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e454-117">CommonParameters</span></span>
<span data-ttu-id="8e454-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e454-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e454-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e454-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e454-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e454-120">INPUTS</span></span>

### <span data-ttu-id="8e454-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8e454-121">System.String</span></span>

## <span data-ttu-id="8e454-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e454-122">OUTPUTS</span></span>

### <span data-ttu-id="8e454-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e454-123">System.Boolean</span></span>

## <span data-ttu-id="8e454-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e454-124">NOTES</span></span>
<span data-ttu-id="8e454-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="8e454-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="8e454-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e454-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e454-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e454-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="8e454-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e454-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
