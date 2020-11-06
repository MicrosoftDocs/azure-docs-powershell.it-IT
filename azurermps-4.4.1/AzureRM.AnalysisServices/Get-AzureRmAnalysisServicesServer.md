---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f80f3eead528c7731007bcd6611f5d6fecbb55e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510791"
---
# <span data-ttu-id="99cb0-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="99cb0-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="99cb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="99cb0-103">Ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="99cb0-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99cb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99cb0-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99cb0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99cb0-105">DESCRIPTION</span></span>
<span data-ttu-id="99cb0-106">Il cmdlet Get-AzureRmAnalysisServicesServer ottiene i dettagli di un server di Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="99cb0-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="99cb0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99cb0-107">EXAMPLES</span></span>

### <span data-ttu-id="99cb0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99cb0-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="99cb0-109">Questo comando consente di ottenere tutti i server di Analysis Services di Azure nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="99cb0-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="99cb0-110">Esempio 2: ottenere un server</span><span class="sxs-lookup"><span data-stu-id="99cb0-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="99cb0-111">Questo comando consente di ottenere il server di Analysis Services di Azure denominato TestServer nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="99cb0-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="99cb0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99cb0-112">PARAMETERS</span></span>

### <span data-ttu-id="99cb0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="99cb0-113">-Name</span></span>
<span data-ttu-id="99cb0-114">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="99cb0-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="99cb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99cb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="99cb0-116">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="99cb0-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="99cb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cb0-117">-DefaultProfile</span></span>
<span data-ttu-id="99cb0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99cb0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99cb0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cb0-119">CommonParameters</span></span>
<span data-ttu-id="99cb0-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99cb0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cb0-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99cb0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cb0-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99cb0-122">INPUTS</span></span>

## <span data-ttu-id="99cb0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99cb0-123">OUTPUTS</span></span>

### <span data-ttu-id="99cb0-124">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="99cb0-124">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="99cb0-125">Note</span><span class="sxs-lookup"><span data-stu-id="99cb0-125">NOTES</span></span>
<span data-ttu-id="99cb0-126">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="99cb0-126">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="99cb0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99cb0-127">RELATED LINKS</span></span>

[<span data-ttu-id="99cb0-128">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="99cb0-128">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="99cb0-129">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="99cb0-129">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
