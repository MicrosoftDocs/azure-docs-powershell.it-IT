---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190635"
---
# <span data-ttu-id="5d85c-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5d85c-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="5d85c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d85c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d85c-103">Ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="5d85c-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="5d85c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d85c-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d85c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d85c-105">DESCRIPTION</span></span>
<span data-ttu-id="5d85c-106">Il cmdlet Get-AzAnalysisServicesServer ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="5d85c-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="5d85c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d85c-107">EXAMPLES</span></span>

### <span data-ttu-id="5d85c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d85c-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="5d85c-109">Questo comando consente di ottenere tutti i server di Analysis Services di Azure nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="5d85c-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="5d85c-110">Esempio 2: ottenere un server</span><span class="sxs-lookup"><span data-stu-id="5d85c-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="5d85c-111">Questo comando consente di ottenere il server di Analysis Services di Azure denominato TestServer nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="5d85c-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="5d85c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d85c-112">PARAMETERS</span></span>

### <span data-ttu-id="5d85c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d85c-113">-DefaultProfile</span></span>
<span data-ttu-id="5d85c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d85c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d85c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d85c-115">-Name</span></span>
<span data-ttu-id="5d85c-116">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5d85c-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="5d85c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d85c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d85c-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="5d85c-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d85c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d85c-119">CommonParameters</span></span>
<span data-ttu-id="5d85c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d85c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d85c-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d85c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d85c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d85c-122">INPUTS</span></span>

### <span data-ttu-id="5d85c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5d85c-123">System.String</span></span>

## <span data-ttu-id="5d85c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d85c-124">OUTPUTS</span></span>

### <span data-ttu-id="5d85c-125">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5d85c-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="5d85c-126">Note</span><span class="sxs-lookup"><span data-stu-id="5d85c-126">NOTES</span></span>
<span data-ttu-id="5d85c-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="5d85c-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="5d85c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d85c-128">RELATED LINKS</span></span>

[<span data-ttu-id="5d85c-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="5d85c-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="5d85c-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="5d85c-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
