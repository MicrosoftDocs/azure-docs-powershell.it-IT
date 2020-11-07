---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 7298612cf64b4f90f65ebaa2943b38102b5ae1ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676106"
---
# <span data-ttu-id="6b9d3-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6b9d3-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="6b9d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9d3-103">Verifica l'esistenza di un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="6b9d3-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="6b9d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b9d3-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b9d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9d3-106">Il cmdlet Test-AzAnalysisServicesServer verifica l'esistenza di un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="6b9d3-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="6b9d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b9d3-107">EXAMPLES</span></span>

### <span data-ttu-id="6b9d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b9d3-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="6b9d3-109">Questo comando testerà se esiste un server denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="6b9d3-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="6b9d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b9d3-110">PARAMETERS</span></span>

### <span data-ttu-id="6b9d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9d3-111">-DefaultProfile</span></span>
<span data-ttu-id="6b9d3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b9d3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b9d3-113">-Name</span></span>
<span data-ttu-id="6b9d3-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6b9d3-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="6b9d3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9d3-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b9d3-116">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="6b9d3-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="6b9d3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9d3-117">CommonParameters</span></span>
<span data-ttu-id="6b9d3-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9d3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9d3-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b9d3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9d3-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b9d3-120">INPUTS</span></span>

### <span data-ttu-id="6b9d3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6b9d3-121">System.String</span></span>

## <span data-ttu-id="6b9d3-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b9d3-122">OUTPUTS</span></span>

### <span data-ttu-id="6b9d3-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b9d3-123">System.Boolean</span></span>

## <span data-ttu-id="6b9d3-124">Note</span><span class="sxs-lookup"><span data-stu-id="6b9d3-124">NOTES</span></span>
<span data-ttu-id="6b9d3-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="6b9d3-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="6b9d3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b9d3-126">RELATED LINKS</span></span>

[<span data-ttu-id="6b9d3-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6b9d3-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="6b9d3-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6b9d3-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)