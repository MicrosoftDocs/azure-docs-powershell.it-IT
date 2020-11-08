---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021905"
---
# <span data-ttu-id="ff10b-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ff10b-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="ff10b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff10b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff10b-103">Verifica l'esistenza di un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="ff10b-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="ff10b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff10b-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff10b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff10b-105">DESCRIPTION</span></span>
<span data-ttu-id="ff10b-106">Il cmdlet Test-AzAnalysisServicesServer verifica l'esistenza di un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="ff10b-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="ff10b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff10b-107">EXAMPLES</span></span>

### <span data-ttu-id="ff10b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff10b-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="ff10b-109">Questo comando testerà se esiste un server denominato TestServer nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="ff10b-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="ff10b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff10b-110">PARAMETERS</span></span>

### <span data-ttu-id="ff10b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff10b-111">-DefaultProfile</span></span>
<span data-ttu-id="ff10b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff10b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff10b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff10b-113">-Name</span></span>
<span data-ttu-id="ff10b-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ff10b-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ff10b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff10b-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff10b-116">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="ff10b-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="ff10b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff10b-117">CommonParameters</span></span>
<span data-ttu-id="ff10b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff10b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff10b-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff10b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff10b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff10b-120">INPUTS</span></span>

### <span data-ttu-id="ff10b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ff10b-121">System.String</span></span>

## <span data-ttu-id="ff10b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff10b-122">OUTPUTS</span></span>

### <span data-ttu-id="ff10b-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff10b-123">System.Boolean</span></span>

## <span data-ttu-id="ff10b-124">Note</span><span class="sxs-lookup"><span data-stu-id="ff10b-124">NOTES</span></span>
<span data-ttu-id="ff10b-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="ff10b-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="ff10b-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff10b-126">RELATED LINKS</span></span>

[<span data-ttu-id="ff10b-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ff10b-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="ff10b-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ff10b-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
