---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: efd4c4770bb9a2628530f476d44e9774534ceee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514000"
---
# <span data-ttu-id="9cbec-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9cbec-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="9cbec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cbec-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbec-103">Ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="9cbec-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cbec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cbec-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cbec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cbec-105">DESCRIPTION</span></span>
<span data-ttu-id="9cbec-106">Il cmdlet Get-AzureRmAnalysisServicesServer ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="9cbec-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="9cbec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cbec-107">EXAMPLES</span></span>

### <span data-ttu-id="9cbec-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9cbec-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="9cbec-109">Questo comando consente di ottenere tutti i server di Analysis Services di Azure nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="9cbec-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="9cbec-110">Esempio 2: ottenere un server</span><span class="sxs-lookup"><span data-stu-id="9cbec-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="9cbec-111">Questo comando consente di ottenere il server di Analysis Services di Azure denominato TestServer nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="9cbec-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="9cbec-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cbec-112">PARAMETERS</span></span>

### <span data-ttu-id="9cbec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbec-113">-DefaultProfile</span></span>
<span data-ttu-id="9cbec-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbec-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cbec-115">-Name</span></span>
<span data-ttu-id="9cbec-116">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9cbec-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9cbec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbec-117">-ResourceGroupName</span></span>
<span data-ttu-id="9cbec-118">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="9cbec-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9cbec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbec-119">CommonParameters</span></span>
<span data-ttu-id="9cbec-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbec-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cbec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbec-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cbec-122">INPUTS</span></span>

### <span data-ttu-id="9cbec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbec-123">System.String</span></span>

## <span data-ttu-id="9cbec-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cbec-124">OUTPUTS</span></span>

### <span data-ttu-id="9cbec-125">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9cbec-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="9cbec-126">Note</span><span class="sxs-lookup"><span data-stu-id="9cbec-126">NOTES</span></span>
<span data-ttu-id="9cbec-127">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="9cbec-127">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="9cbec-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cbec-128">RELATED LINKS</span></span>

[<span data-ttu-id="9cbec-129">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="9cbec-129">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="9cbec-130">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="9cbec-130">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
