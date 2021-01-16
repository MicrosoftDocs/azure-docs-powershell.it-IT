---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368490"
---
# <span data-ttu-id="84b85-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="84b85-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="84b85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84b85-102">SYNOPSIS</span></span>
<span data-ttu-id="84b85-103">Recuperare gli elementi da una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="84b85-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="84b85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84b85-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84b85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84b85-105">DESCRIPTION</span></span>
<span data-ttu-id="84b85-106">Recuperare gli elementi da una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="84b85-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="84b85-107">Se non viene specificata una versione di definizione del modello, viene recuperata la versione bozza.</span><span class="sxs-lookup"><span data-stu-id="84b85-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="84b85-108">Nel caso in cui non sia presente una versione bozza, viene restituita la definizione più recente del modello pubblicato.</span><span class="sxs-lookup"><span data-stu-id="84b85-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="84b85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84b85-109">EXAMPLES</span></span>

### <span data-ttu-id="84b85-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84b85-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="84b85-111">Recuperare gli elementi da una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="84b85-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="84b85-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84b85-112">PARAMETERS</span></span>

### <span data-ttu-id="84b85-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="84b85-113">-Blueprint</span></span>
<span data-ttu-id="84b85-114">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="84b85-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b85-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="84b85-115">-BlueprintVersion</span></span>
<span data-ttu-id="84b85-116">Versione del modello per cui recuperare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="84b85-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="84b85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b85-117">-DefaultProfile</span></span>
<span data-ttu-id="84b85-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84b85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b85-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="84b85-119">-Name</span></span>
<span data-ttu-id="84b85-120">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="84b85-120">Name of the artifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b85-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b85-121">CommonParameters</span></span>
<span data-ttu-id="84b85-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b85-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b85-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84b85-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b85-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84b85-124">INPUTS</span></span>

### <span data-ttu-id="84b85-125">System. String</span><span class="sxs-lookup"><span data-stu-id="84b85-125">System.String</span></span>

### <span data-ttu-id="84b85-126">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="84b85-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="84b85-127">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="84b85-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="84b85-128">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="84b85-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="84b85-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84b85-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="84b85-130">System. String []</span><span class="sxs-lookup"><span data-stu-id="84b85-130">System.String[]</span></span>

## <span data-ttu-id="84b85-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84b85-131">OUTPUTS</span></span>

### <span data-ttu-id="84b85-132">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="84b85-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="84b85-133">Note</span><span class="sxs-lookup"><span data-stu-id="84b85-133">NOTES</span></span>

## <span data-ttu-id="84b85-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84b85-134">RELATED LINKS</span></span>
