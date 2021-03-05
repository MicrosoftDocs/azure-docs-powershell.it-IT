---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007117"
---
# <span data-ttu-id="85f77-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="85f77-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="85f77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85f77-102">SYNOPSIS</span></span>
<span data-ttu-id="85f77-103">Ottenere la proprietà NetworkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="85f77-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="85f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85f77-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85f77-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85f77-105">DESCRIPTION</span></span>
<span data-ttu-id="85f77-106">Il cmdlet **Get-AzCognitiveServicesAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="85f77-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="85f77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85f77-107">EXAMPLES</span></span>

### <span data-ttu-id="85f77-108">Esempio 1: Ottenere la proprietà NetworkRule di un account di Servizi cognitivi specificato</span><span class="sxs-lookup"><span data-stu-id="85f77-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="85f77-109">Questo comando ottiene la proprietà NetworkRule di un account di Servizi cognitivi specificato</span><span class="sxs-lookup"><span data-stu-id="85f77-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="85f77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85f77-110">PARAMETERS</span></span>

### <span data-ttu-id="85f77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f77-111">-DefaultProfile</span></span>
<span data-ttu-id="85f77-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85f77-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f77-113">-Name</span><span class="sxs-lookup"><span data-stu-id="85f77-113">-Name</span></span>
<span data-ttu-id="85f77-114">Nome account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="85f77-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f77-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f77-115">-ResourceGroupName</span></span>
<span data-ttu-id="85f77-116">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85f77-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="85f77-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f77-117">CommonParameters</span></span>
<span data-ttu-id="85f77-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f77-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f77-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85f77-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f77-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="85f77-120">INPUTS</span></span>

### <span data-ttu-id="85f77-121">System.String</span><span class="sxs-lookup"><span data-stu-id="85f77-121">System.String</span></span>

## <span data-ttu-id="85f77-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85f77-122">OUTPUTS</span></span>

### <span data-ttu-id="85f77-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="85f77-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="85f77-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="85f77-124">NOTES</span></span>

## <span data-ttu-id="85f77-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85f77-125">RELATED LINKS</span></span>
