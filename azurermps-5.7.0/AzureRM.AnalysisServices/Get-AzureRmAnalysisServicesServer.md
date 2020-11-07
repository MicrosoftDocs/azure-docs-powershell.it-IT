---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f67c22b483b561af8ffcf2ede9bc1e489379c0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686755"
---
# <span data-ttu-id="a7aae-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a7aae-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="a7aae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7aae-102">SYNOPSIS</span></span>
<span data-ttu-id="a7aae-103">Ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="a7aae-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7aae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7aae-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7aae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7aae-105">DESCRIPTION</span></span>
<span data-ttu-id="a7aae-106">Il cmdlet Get-AzureRmAnalysisServicesServer ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="a7aae-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="a7aae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7aae-107">EXAMPLES</span></span>

### <span data-ttu-id="a7aae-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7aae-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="a7aae-109">Questo comando consente di ottenere tutti i server di Analysis Services di Azure nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="a7aae-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="a7aae-110">Esempio 2: ottenere un server</span><span class="sxs-lookup"><span data-stu-id="a7aae-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="a7aae-111">Questo comando consente di ottenere il server di Analysis Services di Azure denominato TestServer nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="a7aae-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="a7aae-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7aae-112">PARAMETERS</span></span>

### <span data-ttu-id="a7aae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7aae-113">-DefaultProfile</span></span>
<span data-ttu-id="a7aae-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7aae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7aae-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7aae-115">-Name</span></span>
<span data-ttu-id="a7aae-116">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a7aae-116">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7aae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7aae-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7aae-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="a7aae-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7aae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7aae-119">CommonParameters</span></span>
<span data-ttu-id="a7aae-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7aae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7aae-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7aae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7aae-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7aae-122">INPUTS</span></span>

### <span data-ttu-id="a7aae-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7aae-123">None</span></span>
<span data-ttu-id="a7aae-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a7aae-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7aae-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7aae-125">OUTPUTS</span></span>

### <span data-ttu-id="a7aae-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a7aae-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="a7aae-127">Note</span><span class="sxs-lookup"><span data-stu-id="a7aae-127">NOTES</span></span>
<span data-ttu-id="a7aae-128">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="a7aae-128">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="a7aae-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7aae-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7aae-130">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="a7aae-130">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="a7aae-131">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="a7aae-131">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
