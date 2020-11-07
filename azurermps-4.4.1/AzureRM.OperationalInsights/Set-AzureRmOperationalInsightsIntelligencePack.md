---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685666"
---
# <span data-ttu-id="3d9fe-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="3d9fe-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="3d9fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9fe-103">Abilita o Disabilita il pacchetto di informazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d9fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d9fe-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d9fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d9fe-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9fe-106">Il cmdlet **set-AzureRmOperationalInsightsIntelligencePack** Abilita l'intelligence Pack specificata se *Enabled* è impostato su $true e lo Disabilita se *Enabled* è impostato su $false.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="3d9fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d9fe-107">EXAMPLES</span></span>

### <span data-ttu-id="3d9fe-108">Esempio 1: impostare i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="3d9fe-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="3d9fe-109">Questo comando Abilita il pacchetto di informazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="3d9fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d9fe-110">PARAMETERS</span></span>

### <span data-ttu-id="3d9fe-111">-Enabled</span><span class="sxs-lookup"><span data-stu-id="3d9fe-111">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9fe-112">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="3d9fe-112">-IntelligencePackName</span></span>
<span data-ttu-id="3d9fe-113">Specifica il nome del pacchetto di intelligence.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-113">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9fe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9fe-114">-ResourceGroupName</span></span>
<span data-ttu-id="3d9fe-115">Specifica il nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3d9fe-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="3d9fe-116">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3d9fe-116">-WorkspaceName</span></span>
<span data-ttu-id="3d9fe-117">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-117">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9fe-118">-DefaultProfile</span></span>
<span data-ttu-id="3d9fe-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d9fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9fe-120">CommonParameters</span></span>
<span data-ttu-id="3d9fe-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9fe-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9fe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9fe-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d9fe-123">INPUTS</span></span>

## <span data-ttu-id="3d9fe-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d9fe-124">OUTPUTS</span></span>

## <span data-ttu-id="3d9fe-125">Note</span><span class="sxs-lookup"><span data-stu-id="3d9fe-125">NOTES</span></span>

## <span data-ttu-id="3d9fe-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d9fe-126">RELATED LINKS</span></span>

[<span data-ttu-id="3d9fe-127">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="3d9fe-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


