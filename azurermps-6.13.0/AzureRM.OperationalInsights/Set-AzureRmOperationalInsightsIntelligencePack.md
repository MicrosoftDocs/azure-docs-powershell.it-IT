---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 0e8335476fc1cb511aaddb5294ea508832a04003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511607"
---
# <span data-ttu-id="e4577-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="e4577-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="e4577-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4577-102">SYNOPSIS</span></span>
<span data-ttu-id="e4577-103">Abilita o Disabilita il pacchetto di informazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="e4577-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4577-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4577-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4577-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4577-105">DESCRIPTION</span></span>
<span data-ttu-id="e4577-106">Il cmdlet **set-AzureRmOperationalInsightsIntelligencePack** Abilita l'intelligence Pack specificata se *Enabled* è impostato su $true e lo Disabilita se *Enabled* è impostato su $false.</span><span class="sxs-lookup"><span data-stu-id="e4577-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="e4577-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4577-107">EXAMPLES</span></span>

### <span data-ttu-id="e4577-108">Esempio 1: impostare i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="e4577-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="e4577-109">Questo comando Abilita il pacchetto di informazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="e4577-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="e4577-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4577-110">PARAMETERS</span></span>

### <span data-ttu-id="e4577-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4577-111">-DefaultProfile</span></span>
<span data-ttu-id="e4577-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e4577-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4577-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e4577-113">-Enabled</span></span>
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

### <span data-ttu-id="e4577-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="e4577-114">-IntelligencePackName</span></span>
<span data-ttu-id="e4577-115">Specifica il nome del pacchetto di intelligence.</span><span class="sxs-lookup"><span data-stu-id="e4577-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="e4577-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4577-116">-ResourceGroupName</span></span>
<span data-ttu-id="e4577-117">Specifica il nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e4577-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="e4577-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e4577-118">-WorkspaceName</span></span>
<span data-ttu-id="e4577-119">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e4577-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="e4577-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4577-120">CommonParameters</span></span>
<span data-ttu-id="e4577-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4577-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4577-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4577-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4577-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4577-123">INPUTS</span></span>

### <span data-ttu-id="e4577-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e4577-124">System.String</span></span>

### <span data-ttu-id="e4577-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4577-125">System.Boolean</span></span>

## <span data-ttu-id="e4577-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4577-126">OUTPUTS</span></span>

### <span data-ttu-id="e4577-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="e4577-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="e4577-128">Note</span><span class="sxs-lookup"><span data-stu-id="e4577-128">NOTES</span></span>

## <span data-ttu-id="e4577-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4577-129">RELATED LINKS</span></span>

[<span data-ttu-id="e4577-130">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="e4577-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


