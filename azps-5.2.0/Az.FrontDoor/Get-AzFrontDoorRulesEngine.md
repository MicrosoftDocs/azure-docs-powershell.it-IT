---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354343"
---
# <span data-ttu-id="f7116-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="f7116-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="f7116-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7116-102">SYNOPSIS</span></span>
<span data-ttu-id="f7116-103">Ottenere le configurazioni del motore regole.</span><span class="sxs-lookup"><span data-stu-id="f7116-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="f7116-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7116-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7116-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7116-105">DESCRIPTION</span></span>
<span data-ttu-id="f7116-106">Il cmdlet **Get-AzFrontDoorRulesEngine** ottiene una configurazione specifica del motore di regole o ottiene tutte le configurazioni del motore di regole associate a uno sportello anteriore.</span><span class="sxs-lookup"><span data-stu-id="f7116-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="f7116-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7116-107">EXAMPLES</span></span>

### <span data-ttu-id="f7116-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7116-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="f7116-109">Ottenere la configurazione del motore di regole specifiche.</span><span class="sxs-lookup"><span data-stu-id="f7116-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="f7116-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f7116-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="f7116-111">Ottenere tutte le configurazioni del motore di regole in una porta principale.</span><span class="sxs-lookup"><span data-stu-id="f7116-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="f7116-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f7116-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="f7116-113">Output previsto quando si ottiene un motore di regole inesistente.</span><span class="sxs-lookup"><span data-stu-id="f7116-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="f7116-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7116-114">PARAMETERS</span></span>

### <span data-ttu-id="f7116-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7116-115">-DefaultProfile</span></span>
<span data-ttu-id="f7116-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7116-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7116-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="f7116-117">-FrontDoorName</span></span>
<span data-ttu-id="f7116-118">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="f7116-118">Front Door name.</span></span>

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

### <span data-ttu-id="f7116-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7116-119">-Name</span></span>
<span data-ttu-id="f7116-120">Nome motore regole.</span><span class="sxs-lookup"><span data-stu-id="f7116-120">Rules engine name.</span></span>

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

### <span data-ttu-id="f7116-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7116-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7116-122">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="f7116-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="f7116-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7116-123">CommonParameters</span></span>
<span data-ttu-id="f7116-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7116-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7116-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7116-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7116-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7116-126">INPUTS</span></span>

### <span data-ttu-id="f7116-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f7116-127">None</span></span>

## <span data-ttu-id="f7116-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7116-128">OUTPUTS</span></span>

### <span data-ttu-id="f7116-129">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="f7116-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="f7116-130">Note</span><span class="sxs-lookup"><span data-stu-id="f7116-130">NOTES</span></span>

## <span data-ttu-id="f7116-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7116-131">RELATED LINKS</span></span>
