---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 62ef80d7af7ce9b9a10a7a18b38fbf5c6f1db562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994263"
---
# <span data-ttu-id="c2cf1-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c2cf1-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="c2cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cf1-103">Ottenere le configurazioni del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="c2cf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2cf1-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2cf1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="c2cf1-106">Il cmdlet **Get-AzFrontDoorRulesStruttore** ottiene una specifica configurazione del motore di regole o tutte le configurazioni dei motori di regole associate a una porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="c2cf1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2cf1-107">EXAMPLES</span></span>

### <span data-ttu-id="c2cf1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2cf1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="c2cf1-109">Ottenere la configurazione del motore di regole specifico.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="c2cf1-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c2cf1-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="c2cf1-111">Tutte le configurazioni dei motori di regole sono sempre anteriore.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="c2cf1-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c2cf1-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="c2cf1-113">Output previsto quando si riceve un motore di regole inesistente.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="c2cf1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2cf1-114">PARAMETERS</span></span>

### <span data-ttu-id="c2cf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cf1-115">-DefaultProfile</span></span>
<span data-ttu-id="c2cf1-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2cf1-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c2cf1-117">-FrontDoorName</span></span>
<span data-ttu-id="c2cf1-118">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cf1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c2cf1-119">-Name</span></span>
<span data-ttu-id="c2cf1-120">Nome del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-120">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cf1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2cf1-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2cf1-122">Nome del gruppo di risorse con cui verrà creata la porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cf1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cf1-123">CommonParameters</span></span>
<span data-ttu-id="c2cf1-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cf1-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2cf1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cf1-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2cf1-126">INPUTS</span></span>

### <span data-ttu-id="c2cf1-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c2cf1-127">None</span></span>

## <span data-ttu-id="c2cf1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2cf1-128">OUTPUTS</span></span>

### <span data-ttu-id="c2cf1-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesGrafo</span><span class="sxs-lookup"><span data-stu-id="c2cf1-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="c2cf1-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2cf1-130">NOTES</span></span>

## <span data-ttu-id="c2cf1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2cf1-131">RELATED LINKS</span></span>
