---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192582"
---
# <span data-ttu-id="d149c-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d149c-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d149c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d149c-102">SYNOPSIS</span></span>
<span data-ttu-id="d149c-103">Recupera i dettagli di un server Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="d149c-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="d149c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d149c-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d149c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d149c-105">DESCRIPTION</span></span>
<span data-ttu-id="d149c-106">Il Get-AzAnalysisServicesServer cmdlet recupera i dettagli di un server Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="d149c-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="d149c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d149c-107">EXAMPLES</span></span>

### <span data-ttu-id="d149c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d149c-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="d149c-109">Questo comando recupera tutti i server di Azure Analysis Services nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="d149c-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="d149c-110">Esempio 2: Ottenere un server</span><span class="sxs-lookup"><span data-stu-id="d149c-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="d149c-111">Questo comando recupera il server di Azure Analysis Services denominato testserver nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="d149c-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="d149c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d149c-112">PARAMETERS</span></span>

### <span data-ttu-id="d149c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d149c-113">-DefaultProfile</span></span>
<span data-ttu-id="d149c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d149c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d149c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d149c-115">-Name</span></span>
<span data-ttu-id="d149c-116">Nome del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d149c-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d149c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d149c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d149c-118">Nome del gruppo di risorse di Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="d149c-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="d149c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d149c-119">CommonParameters</span></span>
<span data-ttu-id="d149c-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d149c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d149c-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d149c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d149c-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d149c-122">INPUTS</span></span>

### <span data-ttu-id="d149c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d149c-123">System.String</span></span>

## <span data-ttu-id="d149c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d149c-124">OUTPUTS</span></span>

### <span data-ttu-id="d149c-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d149c-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d149c-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d149c-126">NOTES</span></span>
<span data-ttu-id="d149c-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="d149c-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="d149c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d149c-128">RELATED LINKS</span></span>

[<span data-ttu-id="d149c-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="d149c-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="d149c-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="d149c-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
